# Add Speech SDK

```javascript
npm install microsoft-cognitiveservices-speech-sdk

```

```json
 "dependencies": {
        "@babylonjs/core": "5.0.0-beta.4",
        "@babylonjs/loaders": "5.0.0-beta.4",
        "ammo.js": "github:kripken/ammo.js",
        "axios": "^0.25.0",
        "body-parser": "^1.19.0",
        "express": "^4.17.2",
        "express-pino-logger": "^7.0.0",
        "microsoft-cognitiveservices-speech-sdk": "^1.19.0",
        "universal-cookie": "^4.0.4"
    },
    "devDependencies": {
        "@typescript-eslint/eslint-plugin": "^2.30.0",
        "@typescript-eslint/parser": "^2.30.0",
        "body-parser": "^1.19.0",
        "clean-webpack-plugin": "^3.0.0",
        "dotenv": "^14.2.0",
        "eslint": "^7.32.0",
        "express": "^4.17.1",
        "express-pino-logger": "^5.0.0",
        "file-loader": "^6.2.0",
        "html-webpack-plugin": "^5.5.0",
        "node-env-run": "^4.0.2",
        "nodemon": "^2.0.7",
        "npm-run-all": "^4.1.5",
        "pino-colada": "^2.1.0",
        "source-map-loader": "^3.0.0",
        "ts-loader": "^8.3.0",
        "typescript": "^4.5.2",
        "url-loader": "^4.1.1",
        "webpack": "^5.64.2",
        "webpack-cli": "^4.9.1",
        "webpack-dev-server": "^4.5.0",
        "webpack-merge": "^5.8.0"
    },
    "scripts": {
        "start": "npx webpack serve --config webpack.dev.js",
        "build:dev": "npx webpack --config webpack.dev.js",
        "build": "npx webpack --config webpack.prod.js",
        "server": "node-env-run server --exec nodemon | pino-colada",
        "lint": "npx eslint . --ext .ts,.tsx"
    },
```

```javascript
require("dotenv").config();
const express = require("express");
const axios = require("axios");
const bodyParser = require("body-parser");
const pino = require("express-pino-logger")();

const app = express();
app.use(bodyParser.urlencoded({ extended: false }));
app.use(pino);

app.get("/api/get-speech-token", async (req, res, next) => {
    res.setHeader("Content-Type", "application/json");
    const speechKey = process.env.SPEECH_KEY;
    const speechRegion = process.env.SPEECH_REGION;

    if (
        speechKey === "paste-your-speech-key-here" ||
        speechRegion === "paste-your-speech-region-here"
    ) {
        res.status(400).send(
            "You forgot to add your speech key or region to the .env file."
        );
    } else {
        const headers = {
            headers: {
                "Ocp-Apim-Subscription-Key": speechKey,
                "Content-Type": "application/x-www-form-urlencoded",
            },
        };

        try {
            const url =
                "https://speech-westus-speaker.cognitiveservices.azure.com/sts/v1.0/issuetoken"; //
            const tokenResponse = await axios.post(
                `https://${speechRegion}.api.cognitive.microsoft.com/sts/v1.0/issueToken`,
                null,
                headers
            );
            res.send({ token: tokenResponse.data, region: speechRegion });
        } catch (err) {
            res.status(401).send(
                "There was an error authorizing your speech key."
            );
        }
    }
});

app.listen(3001, () =>
    console.log("Express server is running on localhost:3001")
);

```
