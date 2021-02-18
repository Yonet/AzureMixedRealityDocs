# What could go wrong?

### Can one user access to another user's anchors?

Yes, if you build you can prevent that from happening. You can implement Authentication in your application and check for permission before you respond to an API call for Anchors. [Read more...](%20https://docs.microsoft.com/azure/spatial-anchors/concepts/authentication?tabs=csharp&WT.mc_id=github-mixedrealitycurriculum-ayyonet)

### What effects the accuracy of the Spatial Anchors?

Lighting, people moving arround and the changing environment can reduce the retreivability of the anchors. Finding contrasting colored an unchanged object and starting the session from there would be helpful. 

### I can't retrieve my placed anchors, what can I do?

You can retreive a nearby anchor and ask for the other anchors in a radius. 

### How can I have access to my anchor offline?

You can store your Spatial Cloud Anchors as local anchors in your device.

