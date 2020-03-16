# What could go wrong?

#### What are some of the security issues with Mixed Reality Applications?

Since a Mixed Reality application might have access to the user video stream, developers might be able to  save or share private information about the user. Be mindful of not to save any sensitive data or image anywhere other than users device. Never send sensitive information to any backend. 

#### Why is eye scan data sensitive information?

Iris scan is a more accurate identification method than finger print. Since iris scan data can be used to identify and sing in a user, it should never leave the users device. HoloLens 2 does not send the iris scan to the cloud and does not give access to the data.

#### Why is eye tracking important for users privacy? 

Eye tracking, while a very useful tool to make your application more accessible, it can also be used to collect data about the user's attention and might be used to manipulate the user's attention.

#### Can I open my unity project in the current version, if it is originally saved in an older version?

Unity versions are not backward compatible. If you decide to open a project on a newer version, Unity will try to update your project automatically but it is not guaranteed that the newer version will work with your imported assets. There might be some incompatibilities with your asset or your code and the new version. 

#### What does the Unity Versioning mean and when is it safe to update the Unity version?



