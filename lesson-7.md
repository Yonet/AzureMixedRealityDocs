---
description: Azure Spatial Anchors(ASA) and Backend Services
---

# Lesson 7

## Concepts

### What is a Spatial Anchor?

 Spatial Anchors allows you to place virtual object in a specific place in your real world. Spatial Anchors are available in iOS, Android and HoloLens headsets. [Azure Spatial Anchors](https://docs.microsoft.com/azure/spatial-anchors/overview?WT.mc_id=talksAndWorkshops-github-ayyonet) gives you a way to save and share anchor points in space, so that you can share the virtual objects or information between multiple devices and persist them over time.

### Why use Spatial Anchors? 

Using [Azure Spatial Anchors](https://docs.microsoft.com/azure/spatial-anchors/overview?WT.mc_id=github-mixedrealitycurriculum-ayyonet) allow you to share any information in specific context, time and space. Some of the use cases are having user guides of machinery, inventory information, [way-finding applications](https://docs.microsoft.com/azure/spatial-anchors/concepts/anchor-relationships-way-finding?WT.mc_id=github-mixedrealitycurriculum-ayyonet), educational applications, multi-player games. Having smartphones and having access to the GPS data changed the apps we build and enabled ride sharing and location based recommendation applications. Developing with Azure Spatial Anchors will help you deliver contextual data at the right time and place and will open up new possibilities indoors.

###  **Which devices does Azure Spatial Anchors support?**

Azure Spatial Anchors enables developers to build apps on [HoloLens](https://docs.microsoft.com/azure/spatial-anchors/quickstarts/get-started-hololens?WT.mc_id=github-mixedrealitycurriculum-ayyonet), on[ iOS ](https://docs.microsoft.com/azure/spatial-anchors/quickstarts/get-started-ios?tabs=openproject-swift&WT.mc_id=github-mixedrealitycurriculum-ayyonet)devices with ARKit support, and on [Android](https://docs.microsoft.com/azure/spatial-anchors/quickstarts/get-started-android?tabs=openproject-java&WT.mc_id=github-mixedrealitycurriculum-ayyonet) devices with ARCore support; for iOS and Android this includes both phones and tablets. 

### What do I need to do to make sure Android, iOS and HoloLens are using the same point as my anchor?

Azure Spatial Anchors SDK translate the local Spatial Anchor data into Azure Spatial Anchor format and saves it. Similarly, when a different platform asks for the same Spatial anchor data, the device will receive the anchor in platform's format. 

## Project

### How to sign up for Azure Student Account?

* Go to [Azure For Students page.](https://azure.microsoft.com/en-us/free/students/?WT.mc_id=github-mixedrealitycurriculum-ayyonet)
* Follow the Activate Now link.

### How to create an Azure Spatial Anchor resource?

* Go to[ Azure Portal](%20https://portal.azure.com/?WT.mc_id=github-mixedrealitycurriculum-ayyonet).
*  In the left navigation pane in the Azure portal, select **Create a resource**.
*  Use the search box to search for **Spatial Anchors**.

![Azure Portal Search for Spatial Anchor](.gitbook/assets/portal-search.png)

*  Select **Spatial Anchors**. In the dialog box, select **Create**.
* In the **Spatial Anchors Account** dialog box:
  * Enter a unique resource name, using regular alphanumeric characters.
  * Select the subscription that you want to attach the resource to.
  * Create a resource group by selecting **Create new**. Name it **myResourceGroup** and select **OK**. A [resource group](https://docs.microsoft.com/en-us/azure/azure-resource-manager/management/overview#terminology?WT.mc_id=github-mixedrealitycurriculum-ayyonet) is a logical container into which Azure resources like web apps, databases, and storage accounts are deployed and managed. For example, you can choose to delete the entire resource group in one simple step later.
  * Select a location \(region\) in which to place the resource.
  * Select **New** to begin creating the resource.
*  After the resource is created, Azure Portal will show that your deployment is complete. Click **Go to resource**.

![When deployment is complete, select go to resources.](.gitbook/assets/deployment-complete.png)

*  Then, you can view the resource properties. Copy the resource's **Account ID** value into a text editor because you'll need it later.

![Copy Resource&apos;s Account ID.](.gitbook/assets/view-resource-properties.png)

*  Under **Settings**, select **Key**. Copy the **Primary key** value into a text editor. This value is the `Account Key`. You'll need it later.

![](.gitbook/assets/view-account-key.png)

### How to include Azure Spatial Anchors\(ASA\) SDK to your project?

* Go to [Azure Spatial Anchors samples repo](https://github.com/Azure/azure-spatial-anchors-samples?WT.mc_id=github-mixedrealitycurriculum-ayyonet), [releases tab](https://github.com/Azure/azure-spatial-anchors-samples/releases?WT.mc_id=github-mixedrealitycurriculum-ayyonet).
* Scroll down to assets section and click on AzureSpatialAnchors.unitypackage to download.
* In your Unity project select Assets &gt; Import package &gt; custom package and find the downloaded AzureSpatialAnchors.unitypackage and import all.

![Azure Spatial Anchors SDK Releases](.gitbook/assets/asa.png)



