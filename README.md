# NX Hacker News clone

A Hacker News clone built with [NX](http://nx-framework.com).
It features client-side routing, real-time updates and animations.

## Project structure

You can find a readme in every directory of this project, that explains the code inside it.
The project is structured in the following way.
  - The [src](/src) folder includes the API and the NX components of the app.
  - The source is bundled with [Webpack](https://webpack.github.io/). You can find the simple
    bundling  config in [src](/webpack.config.js).
  - [bundle.js](/bundle.js) is the source code and NX bundled together by Webpack.
  - [index.html](/index.html) imports the bundled source script and has a single
    `<hacker-news>` component in its body, that is an NX component defined in the src folder.
    The bundled source is imported as an async script for faster loading.
  - [404.html](/404.html) is a hackish script to make Single Page Apps work with
    Github Pages hosting. For more information see [this repo](https://github.com/rafrex/spa-github-pages).

## Browser support

NX is a next generation framework, supported only by the latest browsers. It works in the
latest Chrome, Firefox Opera and Edge versions, Safari 10 and iOS 10. It doesn't work in any
version of IE yet. The reason is the heavy usage of unpolyfillabe ES6 Proxies, which
makes the NX data binding and reactivity system really simple with no surprise edge cases.
