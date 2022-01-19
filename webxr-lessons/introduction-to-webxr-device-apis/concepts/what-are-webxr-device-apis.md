# What are WebXR Device APIs?

&#x20;**WebXR** is a group of standards being implemented by the browsers, which are used together to support rendering 3D scenes to hardware designed for Mixed Reality. Mixed Reality devices are presenting virtual worlds (**virtual reality**, or **VR**), or for adding graphical imagery to the real world, (**augmented reality**, or **AR**).&#x20;

The **WebXR Device API** implements the core of the WebXR feature set, managing the selection of output devices, render the 3D scene to the chosen device at the appropriate frame rate, and manage input, such as controllers and hand interactions.

WebXR Device APIs are replacing the deprecated WebVR API. WebVR API was designed with only VR devices in mind. With the addition of new AR headsets and AR capable handheld devices, the WebVR API is deprecated in favor of WebXR Device APIs, that include AR Modules.&#x20;

{% embed url="https://youtu.be/ypSkIYpJjE8" %}
An introduction to WebXR APIs and feature samples
{% endembed %}

* [00:00](https://www.youtube.com/watch?v=ypSkIYpJjE8\&t=0s) Introduction&#x20;
* [01:09](https://www.youtube.com/watch?v=ypSkIYpJjE8\&t=69s) WebXR Device APIs:[ https://github.com/immersive-web/webx... ](https://github.com/immersive-web/webxr/blob/master/explainer.md)
* [02:30](https://www.youtube.com/watch?v=ypSkIYpJjE8\&t=150s) Immersive Devices&#x20;
* [03:59](https://www.youtube.com/watch?v=ypSkIYpJjE8\&t=239s) VR Headsets for Mobile Devices.&#x20;
* [05:09](https://www.youtube.com/watch?v=ypSkIYpJjE8\&t=309s) Oculus Quest&#x20;
* [06:07](https://www.youtube.com/watch?v=ypSkIYpJjE8\&t=367s) Augmented Reality(AR) or Mixed Reality(MR) Headsets&#x20;
* [07:00](https://www.youtube.com/watch?v=ypSkIYpJjE8\&t=420s) WebXR with Mobile Devices&#x20;
* [07:36](https://www.youtube.com/watch?v=ypSkIYpJjE8\&t=456s) Pokemon Go&#x20;
* [08:18](https://www.youtube.com/watch?v=ypSkIYpJjE8\&t=498s) WebVR vs WebXR&#x20;
* [09:43](https://www.youtube.com/watch?v=ypSkIYpJjE8\&t=583s) Virtual Reality on the Web&#x20;
* [10:36](https://www.youtube.com/watch?v=ypSkIYpJjE8\&t=636s) Mozilla Hello WebXR Demo: [https://mixedreality.mozilla.org/hell...](https://www.youtube.com/redirect?redir\_token=QUFFLUhqbmlDSXNZU2k5QklDWnNDV2pRdVBJaTBOUTNnZ3xBQ3Jtc0tuTGw0Z2ZFYUlQcDh5NzlaclhNdkl6UHVqdDUzVXFRdnlhM1lrTVdsQjNIWDRQSWhEZERuVGhfVGppU0JmMS1fQUpOaWZRMEFNeUV5b215RmN3TTBxSHpCM0VqdUxYdl9BVGFNSDhLVzdHcEdHX09JOA%3D%3D\&q=https%3A%2F%2Fmixedreality.mozilla.org%2Fhello-webxr%2F\&v=ypSkIYpJjE8\&event=video\_description)&#x20;
* [11:12](https://www.youtube.com/watch?v=ypSkIYpJjE8\&t=672s) WebXR Features 11: 30 Gamepad API&#x20;
* [12:56](https://www.youtube.com/watch?v=ypSkIYpJjE8\&t=776s) Input Profiles Library&#x20;
* [14:51](https://www.youtube.com/watch?v=ypSkIYpJjE8\&t=891s) WebAR Module&#x20;
* [15:50](https://www.youtube.com/watch?v=ypSkIYpJjE8\&t=950s) Hit Test&#x20;
* [17:11](https://www.youtube.com/watch?v=ypSkIYpJjE8\&t=1031s) How to Get Started Building WebXR Experiences&#x20;
* [17:25](https://www.youtube.com/watch?v=ypSkIYpJjE8\&t=1045s) WebGL&#x20;
* [18:00](https://www.youtube.com/watch?v=ypSkIYpJjE8\&t=1080s) WebXR Libraries&#x20;
* [18:08](https://www.youtube.com/watch?v=ypSkIYpJjE8\&t=1088s) ThreeJS: [https://threejs.org/](https://www.youtube.com/redirect?redir\_token=QUFFLUhqbkJKMGZ4aWdNTnR3VnBTNFRQWTJxR21tWHhxZ3xBQ3Jtc0trWlp1TWF0LXNRdXdKSFhCRC05THhWUTMwX1Q4MFBrNTJGRHhJWEJ6SExrRlJXUmdPVUxkaTFRM3hieXFiWF9LV1RDZlFxTFplNHI4VmRmTmJUeUY0bmtKUlNUNERYMW44WFIxTnZqQXF0R1ZLalhMYw%3D%3D\&q=https%3A%2F%2Fthreejs.org%2F\&v=ypSkIYpJjE8\&event=video\_description)&#x20;
* [18:17](https://www.youtube.com/watch?v=ypSkIYpJjE8\&t=1097s) A-Frame: [https://aframe.io/](https://www.youtube.com/redirect?redir\_token=QUFFLUhqbUVOZmNtWElYMFVXTnFLM0RCdzh3RE1HQnZBQXxBQ3Jtc0ttbkp3eXZiNkFLV3VaQU1lU3NoeVg3dGxTcDVKOHFvaXE1UG9ucnZ5SHI3Ym9RQXZkUTFtYkJqdWFDTElRM1AwYUg5X3ZXMF9kYVd0ZzBfN0ItTXVMOGpTSWpFMjg0ZEl5UEdLcUs1R0c4TmR0bnVNMA%3D%3D\&q=https%3A%2F%2Faframe.io%2F\&v=ypSkIYpJjE8\&event=video\_description)&#x20;
* [18:26](https://www.youtube.com/watch?v=ypSkIYpJjE8\&t=1106s) BabylonJS: [https://www.babylonjs.com/](https://www.youtube.com/redirect?redir\_token=QUFFLUhqbmtUZzBJWXpHUjROcGN1c1BFMkUyTEN0cF9Fd3xBQ3Jtc0ttQ1JwazNNX0gtNUU5ZUZUNGVKaDNqSEFhWmlHV0plNzZZNmZWOWdybjFnalZaZURFVHNUNHFlU0ZSQk5td24yU01ZajNWU3hhNXNMeVRDZ2hQYjlzNHpBYWJ4U3hmWkU2M1J0emRlS25DZGJiZUg3cw%3D%3D\&q=https%3A%2F%2Fwww.babylonjs.com%2F\&v=ypSkIYpJjE8\&event=video\_description)&#x20;
* [18:37](https://www.youtube.com/watch?v=ypSkIYpJjE8\&t=1117s) React 360: [https://facebook.github.io/react-360/](https://www.youtube.com/redirect?redir\_token=QUFFLUhqbUlveTJCRkNjb01VVjAtdVBQUDNhRnV6NUgyQXxBQ3Jtc0tsclFfb3hldmtKZ19TZUJGTGZ1Wm1KcUZ2c3Y1V0FQdjRfMW1TSFNMdUMwVW5zVG5CZTdSVGlUVnp2bE1SNlYyTnU3WndKZk92aW0xS0I0ZVM5Uy04QV9Ea0piMjkwSDliQm1lZHNtbllzVVFodXZfUQ%3D%3D\&q=https%3A%2F%2Ffacebook.github.io%2Freact-360%2F\&v=ypSkIYpJjE8\&event=video\_description)&#x20;
* [18:53](https://www.youtube.com/watch?v=ypSkIYpJjE8\&t=1133s) PlayCanvas: [https://playcanvas.com/](https://www.youtube.com/redirect?redir\_token=QUFFLUhqbE53UHJqZDM3aDQtSVgtaGtpSk5XZGo2dVNsQXxBQ3Jtc0ttbG1pcC1JOTg2TFNTOWJ6WVlWY3pJQlJmZU9aUWtJLVpqWmZkUEZRVEhWSXNKUVV3VUJuTWxzN2E3T29ISWtiNHZMZmJmX2VCUlU1bTdzQmhhNWpEbmZPaThfQU5QT09fMDV6RF9rZHppeGRmbjJlZw%3D%3D\&q=https%3A%2F%2Fplaycanvas.com%2F\&v=ypSkIYpJjE8\&event=video\_description)&#x20;
* [19:00](https://www.youtube.com/watch?v=ypSkIYpJjE8\&t=1140s) More on A-Frame&#x20;
* [19:55](https://www.youtube.com/watch?v=ypSkIYpJjE8\&t=1195s) A-Frame Hello World Code&#x20;
* [21:07](https://www.youtube.com/watch?v=ypSkIYpJjE8\&t=1267s) Future of WebXR APIs&#x20;
* [21:29](https://www.youtube.com/watch?v=ypSkIYpJjE8\&t=1289s) WebXR Accessibility and DOM Overlay API&#x20;
* [24:13](https://www.youtube.com/watch?v=ypSkIYpJjE8\&t=1453s) Lighting Estimation Using Computer Vision&#x20;
* [25:05](https://www.youtube.com/watch?v=ypSkIYpJjE8\&t=1505s) Anchors&#x20;
* [26:42](https://www.youtube.com/watch?v=ypSkIYpJjE8\&t=1602s) Layers&#x20;
* [28:16](https://www.youtube.com/watch?v=ypSkIYpJjE8\&t=1696s) Hand Interactions&#x20;
* [29:10](https://www.youtube.com/watch?v=ypSkIYpJjE8\&t=1750s) WebXR Resources 30: 10 How to Get Involved with Immersive Web Working and Community Groups
