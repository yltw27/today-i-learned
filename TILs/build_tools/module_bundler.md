# Webpack

Module bundler is a tool that bundle modules into a single file, which can be shipped and executed in the browser.

Webpack is a module bundler that can digest various module types, like ES modules, common JS modules, AMD modules, CSS import, image url.

Core concepts:

- Entry point: webpack will build a dependency graph starts from this file

- Output: resulting JavaScript files, part of the bundle

- Loaders: 3rd-party extensions that transform different file extensions (e.g. CSS, images, txt) to modules, which can be used as a dependency

- Plugins: 3rd-party extensions that can alter how webpack works

- Mode: webpack has 2 modes (development, production). The main difference is that production mode automatically applies optimization to your code, such as minification

- Code splitting/Lazy loading: split bundles into chunks, which reduces the initial load time as it only loads what's needed at first, then loads other resources on demand

- html-webpack-plugin: a plugin that loads the HTML file and inject bundles to the file
