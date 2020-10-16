# What is the Lifecycle of a WebXR Application?

The basic steps most WebXR applications will go through are:

1. **Query** to see if the desired XR mode is supported.
2. If support is available, **advertise XR functionality** to the user.
3. A [user-activation event](https://html.spec.whatwg.org/multipage/interaction.html#activation) indicates that the user wishes to use XR.
4. **Request an immersive session** from the device
5. Use the session to **run a render loop** that produces graphical frames to be displayed on the XR device.
6. Continue **producing frames** until the user indicates that they wish to exit XR mode.
7. **End the XR session**.

