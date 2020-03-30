# How to contribute?

## Ways to contribute.

Becoming a super hero is a fairly straight forward process:

* You can ****[**file an issue**](https://help.github.com/en/github/managing-your-work-on-github/creating-an-issue) or add a feature request on the curriculum repository: [https://github.com/Yonet/AzureMixedRealityDocs/issues](https://github.com/Yonet/AzureMixedRealityDocs/issues)
* File an issue for the **samples repo**: [https://github.com/Yonet/MixedRealityUnitySamples/issues](https://github.com/Yonet/MixedRealityUnitySamples/issues)
* Add to **curriculum content**: [https://github.com/Yonet/AzureMixedRealityDocs](https://github.com/Yonet/AzureMixedRealityDocs).

### Contributing to content and sample project.

If you have a code sample please either start your code sample from the [HoloLens Seed project](http://bit.ly/HoloLensUnitySeed) or directly  contribute to [Unity Samples repo](http://bit.ly/MixedRealityUnitySamples) by sending a [**pull request.**](https://help.github.com/en/github/collaborating-with-issues-and-pull-requests/proposing-changes-to-your-work-with-pull-requests) You can find the installation information in the related repositories README file.

If you are contributing to Unity Samples, please

1. Fork the [Samples repo](https://github.com/Yonet/MixedRealityUnitySamples) and [curriculum content](https://github.com/Yonet/AzureMixedRealityDocs).
2. Create a branch and name your branch same as the lesson the code example is for. Ex: [Lesson 3: How to add hand interactions to an object?](lessons/lesson-3/project/how-to-place-an-object-onto-a-surface.md), name your branch **03-hand-interaction**. 

   ```text
   //branch-name  = <lesson>-<subtitle>
   git checkout -b branch-name master
   ```

3. Add the changes you want to make. Please follow the structure of the [content explained here](./#how-to-use-this-book).
   1. Every lesson has, [**concepts**,](lessons/lesson1/concepts/)[ **project**](lessons/lesson1/project/), ****[**what could go wrong**](lessons/lesson1/what-could-go-wrong.md) and ****[**resources**](lessons/lesson1/mixed-reality-resources.md) sub-sections.
   2. Every sub-section is divided into [questions](lessons/lesson1/project/how-to-get-started-with-mixed-reality-development-using-unity.md). Please keep the questions and answers precise. If there is another concept you need to explain, **add a new page for the question**.
   3. Questions are meant to follow the top down order and answer the questions necessary to develop the project. Make sure any new questions make sense for the whole of the **hands on project** and **does not diverge into peripheral topics**. Feel free to add the peripheral topics to **Resources** section, [Core concepts](core-building-blocks/) section or file an issue to discuss if the subject is necessary learning.
   4. If you are including a word or a concepts that a person new to Mixed Reality or development in general, please include it in [Glossary ](glossary/)section.
4. If you have images,[ add them in the related folder](https://github.com/Yonet/AzureMixedRealityDocs/tree/master/.gitbook/assets) or create a new folder. Ex:   [.gitbook/assets/how\_to\_add\_audio\_feedback/audio\_source.PNG](https://github.com/Yonet/AzureMixedRealityDocs/pull/4/files#diff-baba7daa2efe95899a805ccdacd9f50d).
5. Make sure to **rebase from master branch** _daily_ and before submitting your pull requests. 

   To rebase your branch and force push to your GitHub repository \(this will update your Pull Request\):

   ```text
   git rebase master -i
   git push -f
   ```

6. Write meaningful commit messages. 
7. [Make a pull request](https://help.github.com/en/github/collaborating-with-issues-and-pull-requests/creating-a-pull-request) to [the upstream master](https://github.com/Yonet/MixedRealityUnitySamples) when you are done with your changes.



```text
Thank you for being our hero!
```

