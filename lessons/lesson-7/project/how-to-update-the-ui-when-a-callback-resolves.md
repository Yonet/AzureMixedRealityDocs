# How to update the UI when a callback resolves?

When working with Unity, all Unity APIs, for example APIs you use to do UI updates, need to happen on the main thread. In the code we'll write however, we get callbacks on other threads. We want to update UI in these callbacks, so we need a way to go from a side thread onto the main thread. To execute code on the main thread from a side thread, we'll use the dispatcher pattern.

* Let's add a member variable, dispatchQueue, which is a Queue of Actions. We will push Actions onto the queue, and then dequeue and run the Actions on the main thread.

```csharp
/// <summary>
/// Set this string to the Spatial Anchors account key provided in the Spatial Anchors resource.
/// </summary>
protected string SpatialAnchorsAccountKey = "Set me";

/// <summary>
/// Our queue of actions that will be executed on the main thread.
/// </summary>
private readonly Queue<Action> dispatchQueue = new Queue<Action>();

/// <summary>
/// Use the recognizer to detect air taps.
/// </summary>
private GestureRecognizer recognizer;
```

* Next, let's add a way to add an Action to the Queue. Add `QueueOnUpdate()` right after `Update()` :

```csharp
/// <summary>
/// Queues the specified <see cref="Action"/> on update.
/// </summary>
/// <param name="updateAction">The update action.</param>
protected void QueueOnUpdate(Action updateAction)
{
    lock (dispatchQueue)
    {
        dispatchQueue.Enqueue(updateAction);
    }
}
```

* Let's now use the Update\(\) loop to check if there is an Action queued. If so, we will dequeue the action and run it.

```csharp
// Update is called once per frame
void Update()
{
    lock (dispatchQueue)
    {
        if (dispatchQueue.Count > 0)
        {
            dispatchQueue.Dequeue()();
        }
    }
}
```

