# What information about an environment is transmitted and stored on the ASA service?

When creating or locating anchors, pictures of the environment are processed on the device into a derived format. This derived format is transmitted to and stored on the service.

To provide transparency, below is an image of an environment and the derived sparse point cloud. The point cloud shows the geometric representation of the environment that's transmitted and stored on the service. For each point in the sparse point cloud, we transmit and store a hash of the visual characteristics of that point. The hash is derived from, but does not contain, any pixel data.

![An environment and its derived sparse point cloud.](../../../.gitbook/assets/asapointcloud.png)

[https://www.youtube.com/watch?v=uwPjlqs8DqE](
https://www.youtube.com/watch?v=uwPjlqs8DqE)

