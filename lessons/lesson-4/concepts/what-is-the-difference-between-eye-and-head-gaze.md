# What's the difference between eye and head gaze?

**Head-gaze** is based on based on the direction that the head/camera is looking at. Head gaze is active on systems that don't support eye gaze, or in cases where the hardware may support eye gaze, but the right set of permissions and setup has not been performed. Think of this as the position and forward direction of the device itself, with the position representing the center point between the two displays. Head gaze is available on both mixed reality and immersive headsets.

**Eye-gaze** is based on where the user's eyes are looking. The origin is located between the user's eyes. It is available on Mixed Reality devices that include an eye tracking system. Eye-gaze is not available on immersive headsets.

Both head and eye-gaze rays are accessible through the **SpatialPointerPose** API. Simply call **SpatialPointerPose::TryGetAtTimestamp** to receive a new SpatialPointerPose object at the specified timestamp and coordinate system. This SpatialPointerPose contains a head-gaze origin and direction. It also contains an eye-gaze origin and direction if eye tracking is available.