# How to Style Bounding Box

Bounding boxes make it easier and more intuitive to manipulate objects with one hand for both near and far interaction by providing handles that can be used for scaling and rotating. A bounding box will show a cube around the hologram to indicate that it can be interacted with. The bounding box also reacts to user input.

![MRTK Bounding Box](../../../.gitbook/assets/how_to_style_bounding_box/mrtk_bounding_box.PNG)

You can add a bounding box to an object by adding the BoundingBox.cs script as a component of the object.

To add the **Bounding Box (Script)** component to an object, first select the object in the Hierarchy window. In the Inspector window, click **Add Component** and search for **Bounding Box**.

![Add Bounding Box Script component](../../../.gitbook/assets/how_to_style_bounding_box/bounding_box_script.PNG)

Select the **Bounding Box** script to apply the component to the object. The bounding box is only visible in Game mode. Press play to view the bounding box. By default, the HoloLens 1st gen style is used.

![View Bounding Box in Game Mode](../../../.gitbook/assets/how_to_style_bounding_box/bounding_box_default.PNG)

To reflect the MRTK bounding box style, you need to change the parameters inside the **Handles** section of the **Bounding Box (Script)** component.

## Change Handle Color

You can change the color of the handles by assigning a material to the **Handle Material** property.

In the **Handles** section, click the circle icon to open the **Select Material** window.

![Change Handle Material parameter](../../../.gitbook/assets/how_to_style_bounding_box/handle_material.PNG)

In the **Select Material** window, search for **BoundingBoxHandleWhite**. Once found, select to assign the color to the handle material.

![Search for BoundingBoxHandleWhite](../../../.gitbook/assets/how_to_style_bounding_box/wireframe_material_pink.PNG)

When you press play, the handle colors for the bounding box will be white.

![New Handle Material](../../../.gitbook/assets/how_to_style_bounding_box/handle_color.PNG)

## Change Handle Color When Object is Grabbed

You can change the color of the handles when an object is grabbed by assigning a material to the **Handle Grabbed Material** property.

In the **Handles** section, click the circle icon to open the **Select Material** window.

![Change Handle Grabbed material](../../../.gitbook/assets/how_to_style_bounding_box/handle_grabbed_parameter.PNG)

In the **Select Material** window, search for **BoundingBoxHandleBlueGrabbed**. Once found, select to assign the color to the handle material.

![Search for BoundingBoxHandleWhite](../../../.gitbook/assets/how_to_style_bounding_box/bounding_box_handle_blue_grabbed.PNG)

When you press play, grab one of the handles of the bounding box. The color of the handle will change to blue.

![New Handle Grabbed material](../../../.gitbook/assets/how_to_style_bounding_box/handle_grabbed_color.PNG)

## Change Scale Handles

You can change the scale handles in corners by assigning a scale handle prefab in the **Scale Handle Prefab** and **Scale Handle Slate Prefab** (for 2D slate) parameters.

First, assign a prefab to the **Scale Handle Prefab**. In the **Handles** section, click the circle icon to open the **Select GameObject** window.

![Open Select GameObject window](../../../.gitbook/assets/how_to_style_bounding_box/select_game_object_window.PNG)

In the **Select GameObject** window, switch to the **Assets** tab and search for **MRTK_BoundingBox_ScaleHandle**. Once found, select to assign the prefab to the scale handle.

![Search for MRTK_BoundingBox_ScaleHandle](../../../.gitbook/assets/how_to_style_bounding_box/scale_handle_prefab.PNG)

Next, assign a prefab to the **Scale Handle Slate Prefab**. In the **Handles** section, click the circle icon to open the **Select GameObject** window.

![Open Select GameObject window](../../../.gitbook/assets/how_to_style_bounding_box/select_game_object_window.PNG)

In the **Select GameObject** window, switch to the **Assets** tab and search for **MRTK_BoundingBox_ScaleHandle_Slate**. Once found, select to assign the prefab to the scale handle.

![Search for MRTK_BoundingBox_ScaleHandle_Slate](../../../.gitbook/assets/how_to_style_bounding_box/scale_handle_slate_prefab.PNG)

When you press play, grab one of the handles of the bounding box to see the change in how the scale handle look.

![New Handle Grabbed material](../../../.gitbook/assets/how_to_style_bounding_box/scale_handle_new.PNG)

## Change Rotation Handles

You can change the rotation handles by assigning a rotation handle prefab in the **Rotation Handle Prefab** parameter.

In the **Handles** section, click the circle icon to open the **Select GameObject** window.

![Open Select GameObject window](../../../.gitbook/assets/how_to_style_bounding_box/rotation_handle_prefab.PNG)

In the **Select GameObject** window, switch to the **Assets** tab and search for **MRTK_BoundingBox_RotateHandle**. Once found, select to assign the prefab to the scale handle.

![Search for MRTK_BoundingBox_RotateHandle](../../../.gitbook/assets/how_to_style_bounding_box/search_rotate_handle.PNG)

When you press play, grab one of the handles of the bounding box to see the change in how the scale handle look.

![New Handle Grabbed material](../../../.gitbook/assets/how_to_style_bounding_box/rotate_handle_new.PNG)