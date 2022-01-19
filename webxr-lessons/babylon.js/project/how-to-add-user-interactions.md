# How to add user interactions?

### Changing color with click event

To change the color of our object with interactions, first we will add a material.

```typescript
    var boxMaterial = new BABYLON.StandardMaterial("material", scene);
    boxMaterial.diffuseColor = BABYLON.Color3.Random();
    box.material = boxMaterial;
```

Now we can add a click event and change the color and position with the click

```typescript
box.actionManager = new BABYLON.ActionManager(scene);
    box.actionManager.registerAction(new BABYLON.ExecuteCodeAction(
    BABYLON.ActionManager.OnPickTrigger, 
    function (evt) {
        var sourceBox = evt.meshUnderPointer;
        
        //move the box upright
        sourceBox.position.x += 0.1;
        sourceBox.position.y += 0.1;

        //update the color
        boxMaterial.diffuseColor = BABYLON.Color3.Random();
    }));
```

{% embed url="https://playground.babylonjs.com/\#KBS9I5\#4103" caption="Playground click event demo" %}

### Dragging an object

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

{% embed url="https://playground.babylonjs.com/\#YEZPVT" %}

Dragging an object in 6 [Degrees of Freedom](https://en.wikipedia.org/wiki/Six_degrees_of_freedom).

{% embed url="https://playground.babylonjs.com/\#5G9MC5" %}

Solution

{% embed url="https://playground.babylonjs.com/\#YEZPVT\#429" %}





