# How to Grab and Move an Object

To grab and move an object, first ensure that the **Manipulation Handler (Script)** and **Near Interaction Grabbable (Script)** components are added to the object. The **Manipulation Handler (Script)** allows you to manipulate an object while the **Near Interaction Grabble (Script) allows the object to respond to near hand interactions.

To add the scripts to the object, first select the object in the Hierarchy window. In the Inspector window, click **Add Component** and search for each script. Once found, select the script to add to the object.

![Add Manipulation Handler Script component](../../../.gitbook/assets/how_to_grab_and_move_an_object/manipulation_handler.PNG)

With the object selected, in the Inspector window, navigate to the **Manipulation Handler (Script)** component to modify the component's parameters.

![Manipulation Handler Parameters](../../../.gitbook/assets/how_to_grab_and_move_an_object/manipulation_handler_parameters.PNG)

You can move an object using one or two hands. This setting is dependent on the **Manipulation Type** parameter. The **Manipulation Type** can be limited to either:
- One Handed Only
- Two Handed Only
- One and Two Handed

Select the preferred **Manipulation Type** so that the user is restricted to use one of the available manipulation types.

![Manipulation Type](../../../.gitbook/assets/how_to_grab_and_move_an_object/manipulation_type.PNG)

note: is there a way to limit just to moving and not move scale or move rotate?