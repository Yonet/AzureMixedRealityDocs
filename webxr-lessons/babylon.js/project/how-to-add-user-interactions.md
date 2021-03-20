# How to add user interactions?

Dragging an object

```typescript
    //Create pointerDragBehavior in the desired mode
    //var pointerDragBehavior = new BABYLON.PointerDragBehavior({});
    //var pointerDragBehavior = new BABYLON.PointerDragBehavior({dragPlaneNormal: new BABYLON.Vector3(0,1,0)});
    var pointerDragBehavior = new BABYLON.PointerDragBehavior({dragAxis: new BABYLON.Vector3(1,0,0)});
    
    // Use drag plane in world space
    pointerDragBehavior.useObjectOrientationForDragging = false;

    // Listen to drag events
    pointerDragBehavior.onDragStartObservable.add((event)=>{
        console.log("dragStart");
        console.log(event);
    })
    pointerDragBehavior.onDragObservable.add((event)=>{
        console.log("drag");
        console.log(event);
    })
    pointerDragBehavior.onDragEndObservable.add((event)=>{
        console.log("dragEnd");
        console.log(event);
    })

    // If handling drag events manually is desired, set move attached to false
    // pointerDragBehavior.moveAttached = false;

    sphere.addBehavior(pointerDragBehavior);
```

{% embed url="https://playground.babylonjs.com/\#5G9MC5" %}



