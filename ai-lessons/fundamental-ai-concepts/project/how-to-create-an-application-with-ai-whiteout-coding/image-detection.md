# How to detect objects from images?

To start creating your AI model for your app, sign in to [Power Apps](https://powerapps.microsoft.com/?WT.mc_id=aiml-8438-ayyonet) and click on AI Builder on the left hand menu. Select Object Detection from the "Refine Model for your business needs" option.

![Build Object Detection on Power Apps - AI Builder](../../../../.gitbook/assets/buildai%20%281%29.png)

Name your new AI model with a unique name. Select Common Objects and proceed to next section.

![Train your custom model screen for Object Detection](../../../../.gitbook/assets/commonobj.png)

Name the objects that you are going to detect. 

![Name each objects to be detected](../../../../.gitbook/assets/namedobjects.png)

Upload images that contain the object you will detect. To start with you can upload **15 images for each object**. 

![Training image format and size for object detection](../../../../.gitbook/assets/imagedetectionformat.png)

Make sure each object has approximately the same amount of images tagged. If you have more examples of one object, the training data will be likely to detect that object when it is not. 

![False positive HoloLens 2 detection](../../../../.gitbook/assets/testresult.png)

Tag your objects by selecting a square that your object is in and choosing the name of the object. 

![Tagging objects](../../../../.gitbook/assets/tagging%20%281%29.png)

Once you are done choose Done Tagging and Train. Training process will take some time.

![You can choose to not use images after you upload and tag them.](../../../../.gitbook/assets/dontuseimage.png)

 If you choose to not use an image or clear any tags, you can do that at any time by going back to your **model** under the **AI Builder** on the left hand side menu and  choose your model and choose edit. 

AI Builder will give you a Performance score over 100 and a way to quickly test your model before publishing. You can edit your models and retrain to improve your performance. Next section will give you some best practices to improve your performance. 

![Performance score of trained model](../../../../.gitbook/assets/performance.png)

