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
