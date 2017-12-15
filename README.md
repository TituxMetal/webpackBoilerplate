# Webpack Boilerplate

A boilerplate with webpack, for web projects

Create a project with a full Webpack configuration for different type of project:

* php project
* symfony 4 project
* VueJs project
* Html project

Simply clone this repo and checkout the branch you want

## Features

* Hot reloading for the full project files (including .twig files)
* Compiling and minifying .js and .scss files
* Source map and versioning in a json file

## Symfony project

### Checkout on the symfony branch

    git checkout symfony

### Install the php dependencies

    make install

    // or via composer
    composer install

### Install node dependencies with yarn or npm

    yarn

    // I like the yarn command, but if you prefer npm...
    npm install

### Start the php server

The php server listen on the hostname 0.0.0.0 and port 8888

If you want to change the hostname and/or the port, update the build/config.js file and pass the HOST and/or the PORT variable to the make command

    make serverStart

    // or via Symfony command
    php bin/console server:start

    // Start the server on localhost:8000
    make serverStart HOST=localhost PORT=8000

### Start the front-end server

    make watch

The front-end server listen on the hostname 0.0.0.0 and port 3000.

If you want to change the hostname and/or the port, update the build/config.js file

### Build the files for production

    make build

All the files go into the public/build directory, css files in css subdirectory and js files in js subdirectory, they are all minified and versionned.

The symfony asset bundle is installed from composer dependencies and the configuration is ready to go. See the templates/demo/index.html.twig file.

The path to the correct version of the file will be automatically inserted, thanks to the manifest.json file generated during the build.

### Start coding

Open your browser with localhost:3000 (or your.host.name:yourFrontendPort) in the url and start coding!

#### And voila, everything is ready for well coding

Every time you change your code, the changes will be compiled and you will see the changes directly in your browser!
