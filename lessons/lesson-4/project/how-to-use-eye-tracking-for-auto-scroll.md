# How to Use Eye-tracking for Auto Scroll

Auto scroll enables the user to scroll through texts without lifting a finger. As the user reads, the text automatically scrolls up or down depending on where the user is looking. In this project, you will create an object that contains a passage of text. As the user reads the text, the text will automatically scroll using eye-tracking data.

First, create an empty game object to organize all the objects together for this project. In the Hierarchy window, right click on an empty space and select **Create Empty**. Name the empty game object **Auto Scroll** and set the **Transform Position** to x = 0, y = 0, z = 2.

![Device System Settings](../../../.gitbook/assets/how-to-use-eye-tracking-for-auto-scroll/create_empty_game_object.png)

Next, create a surface for the text. In the Hierarchy window, select the **Auto Scroll** object. Right click on the object and select **3D Object** > **Quad**. This will create a Quad GameObject as a child of **Auto Scroll**.

![Create Quad GameObject](../../../.gitbook/assets/how-to-use-eye-tracking-for-auto-scroll/create_quad.png)

In the Hierarchy window, select the **Quad** object. In the Inspector window, change the Quad **Transform** parameters to the following:

- **Position**: x = 0, y = 0, z = 0.02
- **Rotation**: x = 0, y = 0, z = 0
- **Scale**: x = 0.6, y = 0.5, z = 0.02

![Quad Transform](../../../.gitbook/assets/how-to-use-eye-tracking-for-auto-scroll/quad_transform.png)

You can add a background color to the Quad object by adding a material component to the object. In the Hierarchy window, select the Quad object. In the Project window, search for **HolographicBackPlateNoBorder**. Once found, drag the **HolographicBackPlateNoBorder** material onto the **Quad** object.

![Search for HolographicBackPlateNoBorder](../../../.gitbook/assets/how-to-use-eye-tracking-for-auto-scroll/add_backplate.png)

In the Scene window, the Quad object's color should be blue.

![Blue Quad](../../../.gitbook/assets/how-to-use-eye-tracking-for-auto-scroll/blue_quad.png)

Next, create a canvas for the text that will display on the Quad object. In the Hierarchy window, select the **Auto Scroll** object. Right click on the object and select **UI** > **Canvas**. This will create a Canvas GameObjet as a child of **Auto Scroll**.

![Create Canvas](../../../.gitbook/assets/how-to-use-eye-tracking-for-auto-scroll/canvas.png)

With the **Canvas** object select, in the Inspector window, change **Render Mode** to **World Space**. This parameter determines how the UI is rendered as an object in 3D space.

![Change Render Mode to World Space](../../../.gitbook/assets/how-to-use-eye-tracking-for-auto-scroll/world_space.png)

With the **Canvas** object still selected, in the Inspector window, change the following parameters in the **Rect Transform** component:

- **Position**: x = 0, y = 0, z = 0
- **Width**: 0
- **Height**: 0
- **Anchors Min**: x = 0, y = 0
- **Anchors Max**: x = 0, y = 0
- **Pivot**: x = 0.5, y = 0.5
- **Scale**: x = 0.005, y = 0.005, z = 0.005

These adjustments will align the canvas to display within the shape of the Quad object.

![Change Rect Tranform parameters](../../../.gitbook/assets/how-to-use-eye-tracking-for-auto-scroll/canvas_rect_transform.png)

With the **Canvas** object still selected, right click the object and select **UI** > **Scroll View**. This will create a **Scroll View** GameObject as a child of **Canvas**.

![Create Scroll View GameObject](../../../.gitbook/assets/how-to-use-eye-tracking-for-auto-scroll/scroll_view.png)

With the **Scroll View** object selected, in the Inspector window, change the following parameters in the **Rect Transform** component:

- **Position**: x = 0, y = 0, z = 0
- **Width**: 110
- **Height**: 90
- **Anchors Min**: x = 0.5, y = 0.5
- **Anchors Max**: x = 0.5, y = 0.5
- **Pivot**: x = 0.5, y = 0.5
- **Rotation**: x = 0, y = 0, z = 0
- **Scale**: x = 1, y = 1, z = 1

![Scroll View Rect Transform](../../../.gitbook/assets/how-to-use-eye-tracking-for-auto-scroll/scroll_view_rect_transform_new.png)

These adjustments will align the scroll view region to display within the shape of the Quad object. In addition, un-check the box next to the **Image** component to remove the white background.

![Uncheck Image](../../../.gitbook/assets/how-to-use-eye-tracking-for-auto-scroll/uncheck_image.png)

With the **Scroll View** object still selected, scroll to the **Scroll Rect** component in the Inspector window. Change the following parameters:

- **Content**: **None (Rect Transform)**
- Uncheck the box next to **Horizontal**
- **Movement Type**: **Clamped**

[add image]

The *Scroll View** object is created with 3 child objects:
- Viewport
- Scrollbar Horizontal
- Scrollbar Vertical

The **Viewport** object will contain both an object for the eye gaze region as well as the text that will display on the Quad object. However, the **Viewport** object currently contains a **Content** child object. Right click the **Content** object and select **Delete** as this object will not be needed.

![Delete Content](../../../.gitbook/assets/how-to-use-eye-tracking-for-auto-scroll/delete_content_object.png)

The **Viewport** object should now be empty. First, create an object for the eyg gaze region. In the Hierarchy window, select the **Quad** object. Right click on the object and select **Create Empty**. This will create an empty **GameObject** as a child of **Quad**. Rename the object **ActiveEyeGazeRegion** and drag the object to become the child of **Viewport**.

![Create ActiveGazeRegion GameObject](../../../.gitbook/assets/how-to-use-eye-tracking-for-auto-scroll/active_eye_gaze_region_child.png)

In the Inspector window, change the **Transform Position** for **ActiveEyeGazeRegion** to x = 55, y = -50, z = 0. Also ensure that **Scale** is set to x = 100, y = 100, z = 4.

![Change ActiveEyeGazeRegion Transform Position](../../../.gitbook/assets/how-to-use-eye-tracking-for-auto-scroll/active_eye_gaze_region_transfom.png)

In the Inspector window, click **Add Component** and search for **Box Collider**. Once found, select to add a box collider to the object.

![Add Box Collider component](../../../.gitbook/assets/how-to-use-eye-tracking-for-auto-scroll/box_collider.png)

The **EyeTrackingTarget** and **ScrollRectTransf** scripts will be added to the **ActiveEyeGazeRegion** object. First, add the **EyeTrackingTarget** script. In the Hierarchy window, select the **ActiveEyeGazeRegion** object. In the Inspector window, click **Add Component** and search for **Eye Tracking Target**. Once found, select the script to add the **EyeTrackingTarget (Script)** component to **ActiveEyeGazeRegion**.

![Add Eye Tracking Target Script component](../../../.gitbook/assets/how-to-use-eye-tracking-for-auto-scroll/add_eye_tracking_target.png)

Next, click **Add Component** and search for **Scroll Rect Transf**. Once found, select the script to add the **ScrollRectTransf (Script)** component to **ActiveEyeGazeRegion**.

![Add ActiveEyeGazeRegion Script component](../../../.gitbook/assets/how-to-use-eye-tracking-for-auto-scroll/add_scroll_rect_transf.png)

Now you will add the text to display on the Quad object. In the Hierarchy window, select the **Viewport** object. Right click on the object and select **UI** > **Text - TextMeshPro**. Rename the object **Text**.

![Create Text - TextMeshPro GameObject](../../../.gitbook/assets/how-to-use-eye-tracking-for-auto-scroll/text_child.png)

With the **Text** object selected, in the Inspector window, scroll to the **TextMeshPro - Text (UI)** component. In the **Text** parameter, enter a long passage. A sample passage is provided below:

*What is Mixed Reality?*

*Mixed reality is the result of blending the physical world with the digital world. Mixed reality is the next evolution in human, computer, and environment interaction and unlocks possibilities that before now were restricted to our imaginations. It is made possible by advancements in computer vision, graphical processing power, display technology, and input systems. The term mixed reality was originally introduced in a 1994 paper by Paul Milgram and Fumio Kishino, "A Taxonomy of Mixed Reality Visual Displays." Their paper introduced the concept of the virtuality continuum, and focused on how the categorization of taxonomy applied to displays. Since then, the application of mixed reality goes beyond displays. It also includes environmental input, spatial sound, and location.*

*Environmental input and perception
Over the past several decades, the relationship between human and computer input has been well explored. It even has a widely studied discipline known as human computer interaction or HCI. Human input happens through a variety of means, including keyboards, mice, touch, ink, voice, and even Kinect skeletal tracking.*

*Advancements in sensors and processing are giving rise to a new area of computer input from environments. The interaction between computers and environments is effectively environmental understanding or perception. Hence the API names in Windows that reveal environmental information are called the perception APIs. Environmental input captures things like a person's position in the world (e.g. head tracking), surfaces and boundaries (e.g. spatial mapping and scene understanding), ambient lighting, environmental sound, object recognition, and location.*

![Add text](../../../.gitbook/assets/how-to-use-eye-tracking-for-auto-scroll/add_text.png)

With the **Text** object still selected, in the Inspector window, change the parameters to the following:

- **Width**: 110
- **Font Size** to **4**
- **Vertex Color** to **E2E2E2**
- **Spacing Options > Line** to **40**
- **Overflow** to **Scroll Rect**
- **Margins** to Left = 5, Top = 5, Right = 5, Bottom = 5
- Check the box for **Extra Padding**

![Change Text properties](../../../.gitbook/assets/how-to-use-eye-tracking-for-auto-scroll/text_parameters.png)

Next, with the **Text** object still selected, in the Inspector window, click **Add Component** and search for **Content Size Fitter**. Once found, select and add the **Content Size Fitter** component to the **Text** object.

![Add Content Size Fitter component](../../../.gitbook/assets/how-to-use-eye-tracking-for-auto-scroll/add_content_size_fitter.png)

For the **Content Size Fitter** component, change the **Vertical Fit** to **Preferred Size**.

![Change Vertical Fit to Preferred Size](../../../.gitbook/assets/how-to-use-eye-tracking-for-auto-scroll/vertical_fit.png)

You now need to go back to the **ActiveEyeGazeRegion** object to create events for the **EyeTrackingTarget** component so that eye tracking starts when the user is looking at the target and stops when the user looks away. In the Hierarchy window, select **ActiveEyeGazeRegion**. In the Inspector window, scroll to the **EyeTrackingTarget** component.

Add an **On Look At Start()** event. Assign the **ActiveEyeGazeRegion** object to the event and select **ScrollRectTransf.StartFocusing** as the action.

![Create On Look At Start() event](../../../.gitbook/assets/how-to-use-eye-tracking-for-auto-scroll/on_start_event.png)

Next, add an **On Look Away()** event. Assign the **ActiveEyeGazeRegion** object to the event and select **ScrollRectTransf.StopFocusing** as the action.

![Create On Look Away() event](../../../.gitbook/assets/how-to-use-eye-tracking-for-auto-scroll/on_look_away.png)

Now, you need to assign the **Text** and **Viewport** objects to the **ScrollRectTransf** component. Scroll down to the **ScrollRectTransf** component. Assign the **Text** object to **Rect Transf to Navigate** and **Viewport** to **Ref to View Port**.

![Assign Text and Viewport to ScrollRectTransf component](../../../.gitbook/assets/how-to-use-eye-tracking-for-auto-scroll/assign_to_scrollrectransf.png)

The final step is to change the scroll bars. In the Hierarchy window, select the **Scrollbar Horizontal** object. In the Inspector window, adjust the following settings:

- **Height**: **7**
- Image > **Color**: **525252**
- Scrollbar > Transition > **Normal Color**: **525252**
- Scrollbar > Transition> **Color Multiplier**: **2**

![Scrollbar Horizontal](../../../.gitbook/assets/how-to-use-eye-tracking-for-auto-scroll/sb_horizontal.png)

Next, select the **Scrollbar Vertical** object in the Hierarchy. In the Inspector window, adjust the following settings:

- **Position**: x = 3, y = 0, z = 0
- **Width**: **7**
- Image > **Color**: **525252**
- Scrollbar > Transition > **Normal Color**: **525252**
- Scrollbar > Transition > **Color Multiplier**: **2**
- Scrollbar > **Value**: **0**
- Scrollbar > **Size**: **1**

![Scrollbar Vertical](../../../.gitbook/assets/how-to-use-eye-tracking-for-auto-scroll/sb_vertical.png)

To test your scene using the in-editor simulation, enter Game mode by pressing play. Use the keyboard to zoom in towards the text. Once the text is centered on the scroll, use the keyword to move the camera down. You will notice that the text will start to scroll down. If you move the camera up, the text will start to scroll up.

![Game mode](../../../.gitbook/assets/how-to-use-eye-tracking-for-auto-scroll/game_mode.png)