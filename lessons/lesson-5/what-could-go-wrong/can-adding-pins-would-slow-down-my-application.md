# Can adding pins would slow down my application?

Creating and adding many MapPins at once, either to a MapPinLayer or as children of the MapRenderer, could be time consuming and thus cause a frame hitch. If the MapPins can be initialized and added all at startup, this may be an acceptable one time hit. However, if data is being streamed and converted to MapPins throughout the app's lifetime, consider spreading out the MapPin creation and addition over multiple frames, i.e. time slice the additions. This will help to maintain render performance.

