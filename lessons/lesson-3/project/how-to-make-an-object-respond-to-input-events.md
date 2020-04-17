# How to make an object respond to input events?

An input event is an action in your app that triggers a specific action to occur. For example, you could use speech to trigger an object to change colors. There are several input events that can be used in your app by implementing an event handler. A description of each handler is provided below: <br><br>

|Handler  |Events  |Description  |
|---------|---------|---------|
|IMixedRealitySourcesStateHandler     |    Source Detected / Lost     |   Raised when an input source is detected/lost, like when an articulated hand is detected or lost track of.     |
|IMixedRealitySourcePoseHandler     |     Source Pose Changed    |    Raised on source pose changes. The source pose represents the general pose of the input source. Specific poses, like the grip or pointer pose in a six DOF controller, can be obtained via IMixedRealityInputHandler<MixedRealityPose>.     |
|IMixedRealityInputHandler     |    Input Down / Up     |    Raised on changes to binary inputs like buttons.     |
|IMixedRealityInputHandler<T>     |     Input Changed    |         |
|IMixedRealitySpeechHandler    |    Speech Keyword Recognized     |    Raised on recognition of one of the keywords configured in the Speech Commands Profile.     |
|IMixedRealityDictationHandler     |    Dictation, Hypothesis, Result, Complete, Error     |    Raised by dictation systems to report the results of a dictation session.     |
|IMixedRealityGestureHandler    |    Gesture events on: Started, Updated, Completed, Canceled     |    Raised on gesture detection.     |
|IMixedRealityGestureHandler<T>     |   Gesture Updated / Completed      |     Raised on detection of gestures containing additional data of the given type. See gesture events for details on possible values for T.    |
|IMixedRealityHandJointHandler    |    Hand Joints Updated     |   Raised by articulated hand controllers when hand joints are updated.      |
|IMixedRealityHandMeshHandler     |     Hand Mesh Updated    |    Raised by articulated hand controllers when a hand mesh is updated.     |
|IMixedRealityInputActionHandler     |     Action Started / Ended    |   Raise to indicate action start and end for inputs mapped to actions.      |

To use speech to trigger an objet to rotate, you will need to create a new speech command and then configure the event so it triggers the desired action when the speech command keyword is spoken.

In the Hierarchy window, click the **MixedRealityToolkit** object. In the Inspector window, click **Clone**.

![Clone Configuration profile](../../../.gitbook/assets/clone_configuration_profile.PNG)

In the **Clone Profile** window, click **Clone** to create a configuration new profile.

![Create new Configuration profile](../../../.gitbook/assets/create_new_config_profile.PNG)

In the Inspector window, select **Input** and click **Clone**.

![Clone Input profile](../../../.gitbook/assets/clone_input_profile.PNG)

In the **Clone Profile** window, click **Clone** to create a new Input System profile.

![Create new Input profile](../../../.gitbook/assets/create_new_input_profile.PNG)

Expand the **Speech** section and click **Clone**.

![Clone Speech profile](../../../.gitbook/assets/clone_speech_profile.PNG)

In the **Clone Profile** window, click **Clone** to create a new Speech Commands profile.

![Create new Speech profile](../../../.gitbook/assets/create_new_speech_profile.PNG)

In the **Speech Commands** section, click the **+ Add a New Speech Command** button. This will enable you to add a new speech command to the bottom of the list of existing speech commands.

![Add new Speech Command](../../../.gitbook/assets/add_new_speech_command.PNG)

In the **Keyword** field, enter the phrase **Change Color**.

![Type in a Keyword](../../../.gitbook/assets/keyword.PNG)

If you intend to use the in-editor simulation to test the trigger but do not have a microphone, assign a **KeyCode** using a corresponding key on your keyboard, for example: **C**.

![Select a KeyCode](../../../.gitbook/assets/keycode.PNG)

In the Hierarchy window, select the object that will perform the action. In the Inspector window, click **Add Component** and search for **Speech Input Handler**. Once found, add the **Speech Input Handler (Script)** to the object.

![Manipulation Type](../../../.gitbook/assets/add_component.PNG)

On the **Speech Input Handler (Script)** component, un-check **Is Focus Required**. By unchecking this box, the user is not required to look at the object to trigger the speech command.

![Manipulation Type](../../../.gitbook/assets/is_focus_required.PNG)

On the **Speech Input Handler (Script)** component, click the small **+** button to add a keyword element to the list of keywords.

![Manipulation Type](../../../.gitbook/assets/add_keyword.PNG)

Expand the newly created **Element 0**. Type the new keyword **Change Color** that was created earlier. Unity only allows registered keywords from the **Speech Commands** list in the **Speech Commands Profile**. If you enter a nonregistered keyword, a warning will appear.

![Manipulation Type](../../../.gitbook/assets/type_keyword.PNG)

Click the **+** button to create a new **Response ()** event. Assign the object to the event and define **MeshRender.Materialmaterial** as the action to be triggered. This will enable you to assign a color.

[insert picture]

To assign the color, click the circle for the material (currently **None (Material)**). In the **Select Material** window, search for **MRTK_Standard** to locate the MRTK standard materials. Select a color to assign to the material.

![Manipulation Type](../../../.gitbook/assets/search_mrtk_standard.PNG)

To test the input event using in editor simulation, press the play button to enter Game mode. 

![Object before color change](../../../.gitbook/assets/before_color_change.PNG)

If you have a microphone connected to your computer, say the phrase **Change Color**. If you do not have a microphone connected to your computer, press the **C** key on your keyword.

![Object after color change](../../../.gitbook/assets/color_change.PNG)