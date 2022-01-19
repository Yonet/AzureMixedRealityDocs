# How to style Bounding Box?

Bounding boxes make it easier and more intuitive to manipulate objects with one hand for both near and far interaction by providing handles that can be used for scaling and rotating. A bounding box will show a cube around the hologram to indicate that it can be interacted with. The bounding box also reacts to user input.

![MRTK Bounding Box](../../../.gitbook/assets/mrtk_bounding_box.png)

You can add a bounding box to an object by adding the BoundingBox.cs script as a component of the object.

To add the **Bounding Box \(Script\)** component to an object, first select the object in the Hierarchy window. In the Inspector window, click **Add Component** and search for **Bounding Box**.

![Add Bounding Box Script component](../../../.gitbook/assets/bounding_box_script.png)

Select the **Bounding Box** script to apply the component to the object. The bounding box is only visible in Game mode. Press play to view the bounding box. By default, the HoloLens 1st gen style is used.

![View Bounding Box in Game Mode](../../../.gitbook/assets/bounding_box_default.png)

To reflect the MRTK bounding box style, you need to change the parameters inside the **Handles** section of the **Bounding Box \(Script\)** component.

### Change Handle Color

You can change the color of the handles by assigning a material to the **Handle Material** property.

In the **Handles** section, click the circle icon to open the **Select Material** window.

![Change Handle Material parameter](../../../.gitbook/assets/handle_material.png)

In the **Select Material** window, search for **BoundingBoxHandleWhite**. Once found, select to assign the color to the handle material.

![Search for BoundingBoxHandleWhite](../../../.gitbook/assets/wireframe_material_pink.png)

When you press play, the handle colors for the bounding box will be white.

![New Handle Material](../../../.gitbook/assets/handle_color.png)

### Change Handle Color When Object is Grabbed

You can change the color of the handles when an object is grabbed by assigning a material to the **Handle Grabbed Material** property.

In the **Handles** section, click the circle icon to open the **Select Material** window.

![Change Handle Grabbed material](../../../.gitbook/assets/handle_grabbed_parameter.png)

In the **Select Material** window, search for **BoundingBoxHandleBlueGrabbed**. Once found, select to assign the color to the handle material.

![Search for BoundingBoxHandleWhite](../../../.gitbook/assets/bounding_box_handle_blue_grabbed.png)

When you press play, grab one of the handles of the bounding box. The color of the handle will change to blue.

![New Handle Grabbed material](../../../.gitbook/assets/handle_grabbed_color.png)

### Change Scale Handles

You can change the scale handles in corners by assigning a scale handle prefab in the **Scale Handle Prefab** and **Scale Handle Slate Prefab** \(for 2D slate\) parameters.

First, assign a prefab to the **Scale Handle Prefab**. In the **Handles** section, click the circle icon to open the **Select GameObject** window.

![Open Select GameObject window](../../../.gitbook/assets/select_game_object_window.png)

In the **Select GameObject** window, switch to the **Assets** tab and search for **MRTK\_BoundingBox\_ScaleHandle**. Once found, select to assign the prefab to the scale handle.

![Search for MRTK\_BoundingBox\_ScaleHandle](../../../.gitbook/assets/scale_handle_prefab.png)

Next, assign a prefab to the **Scale Handle Slate Prefab**. In the **Handles** section, click the circle icon to open the **Select GameObject** window.

![Open Select GameObject window](../../../.gitbook/assets/select_game_object_window.png)

In the **Select GameObject** window, switch to the **Assets** tab and search for **MRTK\_BoundingBox\_ScaleHandle\_Slate**. Once found, select to assign the prefab to the scale handle.

![Search for MRTK\_BoundingBox\_ScaleHandle\_Slate](../../../.gitbook/assets/scale_handle_slate_prefab.png)

When you press play, grab one of the handles of the bounding box to see the change in how the scale handle look.

![New Handle Grabbed material](../../../.gitbook/assets/scale_handle_new.png)

### Change Rotation Handles

You can change the rotation handles by assigning a rotation handle prefab in the **Rotation Handle Prefab** parameter.

In the **Handles** section, click the circle icon to open the **Select GameObject** window.

![Open Select GameObject window](../../../.gitbook/assets/rotation_handle_prefab.png)

In the **Select GameObject** window, switch to the **Assets** tab and search for **MRTK\_BoundingBox\_RotateHandle**. Once found, select to assign the prefab to the scale handle.

![Search for MRTK\_BoundingBox\_RotateHandle](../../../.gitbook/assets/search_rotate_handle.png)

When you press play, grab one of the handles of the bounding box to see the change in how the scale handle look.

![New Handle Grabbed material](../../../.gitbook/assets/rotate_handle_new.png)

