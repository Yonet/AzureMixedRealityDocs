# How to Organize Your Objects into a Grid View

You can organize any objects in Unity into a grid by using an **Object collection** script. In this example, you will learn how to organize 6 3D objects into a 3 x 3 grid.

![3 x 3 Grid](../../../.gitbook/assets/how_to_organize_your_objects_into_a_grid_view/grid.PNG)

First, configure your Unity scene for the Mixed Reality Toolkit. Next, in the Hierarchy window, right click in an empty space and select **Create Empty**. This will create an empty GameObject. Name the object **CubeCollection**. 

![Create an empty GameObject](../../../.gitbook/assets/how_to_organize_your_objects_into_a_grid_view/create_empty.PNG)

In the Inspector window, position **CubeCollection** so that the collection displays in front of the user (example, X = 0, Y = -0.2, Z = 2).

![Change Position](../../../.gitbook/assets/how_to_organize_your_objects_into_a_grid_view/position.PNG)

With **CubeCollection** still selected, in the Hierarchy window, create a child **Cube** object. Change the scale of the object to x = .25, y = .25, z = .25.

![Create Scale of Cube](../../../.gitbook/assets/how_to_organize_your_objects_into_a_grid_view/scale_cube.PNG)

Duplicate the child **Cube** object 8 times so that there is a total of 9 **Cube** child objects within the **CubeCollection** object.

![Duplicate Cube GameObject 8 times](../../../.gitbook/assets/how_to_organize_your_objects_into_a_grid_view/duplicate_cubes.PNG)

In the Hierarchy window, select **CubeCollection**. In the Inspector window, click **Add Component** and search for the **Grid Object Collection (Script)**. Once found, select the component to add to the object.

![Add Grid Object Collection Script component](../../../.gitbook/assets/how_to_organize_your_objects_into_a_grid_view/grid_object_collection.PNG)

Configure the **Grid Object Collection (Script)** component by changing the **Sort Type** property to **Child Order**. This will ensure that the child objects (the 9 Cube objects) are sorted in the order you placed them under the parent object.

![Change Sort Type](../../../.gitbook/assets/how_to_organize_your_objects_into_a_grid_view/sort_type.PNG)

Click **Update Collection** to apply the new configuration.

![Update Collection](../../../.gitbook/assets/how_to_organize_your_objects_into_a_grid_view/update_collection.PNG)

You can adjust the parameters within the **Grid Object Collection (Script)** component to further customize the grid. For example, you could change the number of rows to 2 by changing the value in the **Num Rows** properties. Be sure to click **Update Collection** to apply the new configuration.

![Change Num Rows](../../../.gitbook/assets/how_to_organize_your_objects_into_a_grid_view/rows.PNG)