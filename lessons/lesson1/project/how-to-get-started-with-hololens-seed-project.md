# How to get started with HoloLens Seed Project?

\*\*\*\*[**HoloLens Seed** project](https://github.com/Yonet/HoloLensUnitySeedProject) is a github repository that is configured for **Windows Mixed Reality development**. The repo includes **Mixed Reality Toolkit** and **.gitignore** files. 

You can create a new project from the seed instead of downloading the different assets and setting up your git project. To be able to use the seed project, you can [get a github account](https://github.com/?WT.mc_id=github-mixedrealitycurriculum-ayyonet) and setup your development environment or directly download the repository content.

![Download Seed project from github.](../../../.gitbook/assets/downloadseed.png)

## Setup

You can clone and delete this repository's history and start a new git project by running the below script. You need to create your own github repo first. Replace with your own github project url.

```text
git clone --depth=1 https://github.com/Yonet/HoloLensUnitySeedProject.git <your-project-name>
```

Or by running the below github commands:

```text
// Clone the seed project
git clone --depth=1 https://github.com/Yonet/HoloLensUnitySeedProject.git

-- Remove the history from the repo
rm -rf .git

-- recreate the repos from the current content only
git init
git add .
git commit -m "Initial commit"

-- push to the github remote repos ensuring you overwrite history
git remote add origin git@github.com:<YOUR ACCOUNT>/<YOUR REPOS>.git
git push -u --force origin master
```

### How to update your project to latest seed?

 Whenever there is a new update for [Mixed Reality Toolkit](https://microsoft.github.io/MixedRealityToolkit-Unity/README.html?WT.mc_id=hololensseedproject-github-ayyonet) or [Azure Spatial Anchors](https://docs.microsoft.com/azure/spatial-anchors/?WT.mc_id=hololensseedproject-github-ayyonet) packages, this repo will be updated with the latest version. You can automaticly get the latest packages by adding the seed repo as your upstream and pulling from it.

```text
git remote add upstream https://github.com/Yonet/HoloLensUnitySeedProject.git
git pull upstream master
```

You can check to see if your remote origin and upstream by copy and pasting to your terminal:

```text
git remote -v
```

You can remove the upstream anytime by running:

```text
git remote remove upstream https://github.com/Yonet/HoloLensUnitySeedProject.git
```

