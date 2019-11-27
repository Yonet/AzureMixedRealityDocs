# Overview

In this section you will learn how to use Azure Language and Speech Services to add conversational abilites to your VR application.

# Azure Speech Services

[Azure Speech Services](https://docs.microsoft.com/azure/cognitive-services/speech-service/?WT.mc_id=mrdocs-github-academic) are the unification of [speech-to-text](https://docs.microsoft.com/azure/cognitive-services/speech-service/speech-to-text?WT.mc_id=mrdocs-github-academic), [text-to-speech](https://docs.microsoft.com/azure/cognitive-services/speech-service/text-to-speech?WT.mc_id=mrdocs-github-academic), and s[peech-translation](https://docs.microsoft.com/azure/cognitive-services/speech-service/speech-translation?WT.mc_id=mrdocs-github-academic) into a single [Azure subscription](https://azure.microsoft.com/free/?WT.mc_id=mrdocs-github-academic). It's easy to speech enable your applications, tools, and devices with the [Speech SDK](https://docs.microsoft.com/azure/cognitive-services/speech-service/speech-sdk?WT.mc_id=mrdocs-github-academic), [Speech Devices SDK](https://docs.microsoft.com/azure/cognitive-services/Speech-Service/speech-devices-sdk-android-quickstart?WT.mc_id=mrdocs-github-academic), or [REST APIs](https://docs.microsoft.com/azure/cognitive-services/speech-service/overview?WT.mc_id=mrdocs-github-academic#reference-docs).

# Azure Languages Services

Azure Language services allow you to add natural language processing tools to evaluate sentiment, recognize key phrases, create conversational language understanding and learn how to recognize what users want.

## A highlevel of how text is processed in machine learning
Although you will be using prebuilt models from Azure services, its still helpful to understand how a computer processes text to make the responses to a user.

At a high level a "Bag-of-Words" style model is taking the text, removing stop words (such as “the”, “a”, “an”, “in”), applying lemmatization (converts multiple related words to a single form (example: "fruity", "fruitiness" and "fruits" would all become "fruit"), creates a tokenization of the words and then creates a vector of numbers that represents the text. The text is now represented as numbers with only the words we told the model to include and can be processed by the computer to train a model. Remember the computer understand numbers and words can be represented as numbers so the computer can "understand".


# Exercise
Create a Unity/C# VR application with a bot that can answer some basic questions from speech input.

Build a VR game given the [base template]().

1. Use the speech service to capture the users input from the microphone with the speech to text feature.
2. Use the speech service to respond back to the user with the text to speech feature.
3. Build a LUIS model to take action based on the user speech to text input result.
    * The luis model should be able to answer basic questions about it self. Some Examples"
        1. What is your favorite color?
        2. Where are you from?
        3. Do you have a favorite sport?
        4. What is your name?
        5. Tell the robot to move in a direction
        6. Be creative and think of other things a user might ask your bot about itself. 
4. Use the text analytics service to display entities and sentiment from the text received from the user.
