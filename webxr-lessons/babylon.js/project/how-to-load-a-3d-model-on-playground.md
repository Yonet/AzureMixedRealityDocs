# How to load a 3D model on Playground?

Loading a 3D model is like uploading an image but for 3D models. You can upload one or multiple models as shown in below code sample.

```javascript
//empty string all meshes
BABYLON.SceneLoader.ImportMeshAsync("", "/relative path/", "myFile"); 
//Name of model for one model
BABYLON.SceneLoader.ImportMeshAsync("model1", "/relative path/", "myFile"); 
//Array of model names
BABYLON.SceneLoader.ImportMeshAsync(["model1", "model2"], "/relative path/", "myFile"); 
```

Loading takes time and is asynchronous. When we call the function, web browser gives us back a "[Promise](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global\_Objects/Promise)" that it will give us a result when the loading is complete. Now we can call the can let the browser know what we want to do when the loading is complete inside the .then(whatToDoWhenModelLoadedFunction). We call this function a **callback functions**.

Below example loads all the models in the path and changes the position.

```typescript
    BABYLON.SceneLoader.ImportMeshAsync("", "https://assets.babylonjs.com/meshes/", "both_houses_scene.babylon").then((result) => {
        const house1 = scene.getMeshByName("detached_house");
        house1.position.y = 2;
        const house2 = result.meshes[2];
        house2.position.y = 1;
    });
```

{% embed url="https://playground.babylonjs.com/#YNEAUL#13" %}
Playground loading models example
{% endembed %}

### Exercise:

1\) The postion of the house is changed in the above example by setting an integer value to  house1.position.y. Try setting scaling the model by setting it's scale value, ex: **house1.scale.x**.

2\) Console.log the house2 object to see what it is. Save and open the developer tools with the short cut: **Option +  Command + I on mac** and **Control + Shift + I on windows**. Find the console tab to see the printed house object.

```typescript
   BABYLON.SceneLoader.ImportMeshAsync("", "https://assets.babylonjs.com/meshes/", "both_houses_scene.babylon").then((result) => {
        const house1 = scene.getMeshByName("detached_house");
        house1.position.y = 2;
        const house2 = result.meshes[2];
        house2.position.y = 1;
        console.log("House2 is ", house2);
    });
```

