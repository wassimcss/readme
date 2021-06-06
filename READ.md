<p align="center">
  <img alt="Figma to HTML title" height="400" src="https://cdn.builder.io/api/v1/image/assets%2FYJIGb4i01jvw0SRdL5Bt%2F7fbe481d20d74cee827ee7256b37a736" />
</p>

<p align="center">
  Convert Figma designs into high quality HTML, React, Vue, Svelte, Angular, Solid, etc code via <a href="https://github.com/BuilderIO/jsx-lite">JSX Lite</a>
</p>
<br />

<p align="center">
  <img src="https://i.imgur.com/BoKsLFs.gif" />
</p>

## How does it work
### Export design to code 
1. [Install Visual Studio Code](https://code.visualstudio.com/)
2. [Install Node.js and NPM](https://nodejs.org/en/download/)
3. Install TypeScript : run sudo npm install -g typescript in a terminal
4. Get the Figma desktop app : <br/>
   -[For Windows and macOS](https://www.figma.com/downloads/)<br/>
   -[For linux](https://snapcraft.io/figma-linux)
5. Log in to your account and open the file editor in the Figma desktop app,you can open any existing document or create a new one.
6. Go to Menu > Plugins > Development > New Plugin:this will bring up the "Create a plugin" modal to create a sample plugin
7. Choose the file manifest.json from your project
8. Open the code folder you just created using Visual studio code 
9. Install all dependencies : npm install
10. Run npm install --save-dev @figma/plugin-typings in the terminal
10. Run npm run dev:lib
11. Ensure all layers you want to import use autolayout as described [here](https://www.builder.io/c/docs/import-from-figma)
12. Click the "get code" button to launch into the Builder.io editor


### Import webpages to Figma designs


1. In Figma, open a new or existing document, then hit cmd+/ and search "html figma" and hit enter
2. Enter a URL you want to import

<a href="https://github.com/builderio/jsx-lite">
  <img src="https://i.imgur.com/YNDD9dH.gif" alt="Plugin demo" width="480" />
</a>

## Why?

- Instantly convert designs into live webpages and code
- Easily import real live site styles for a starting point for designs and prototypes
- Quickly turn real site components into design components
- Easy import from storybook, etc

## Chrome Extension

Want to capture a page behind an auth wall, or in a specific state you need to navigate to? Then the [chrome extension](https://chrome.google.com/webstore/detail/efjcmgblfpkhbjpkpopkgeomfkokpaim) is for you!

<img src="https://imgur.com/ARz16KC.gif" alt="Chrome extension demo" width="480" />

## Using the library

```js
// npm install @builder.io/html-to-figma
import { htmlToFigma } from "@builder.io/html-to-figma";
const layers = htmlToFigma(document.body);
// E.g. send these to the REST API, or generate a .figma.json file that can be uploaded through the Figma plugin
```

## Limitations

Importing HTML layers to Figma is a best-effort process. Even getting 90% there can save you a ton of time, only having to clean up a few things.

A few known limitations:

- not all element types are supported (e.g. iframe, pseudoelements)
- not all CSS properties are supported or fully supported
- not all types of media are supported (video, animated gifs, etc)
- all fonts have to be uploaded to Figma or a best effort fallback will be used



