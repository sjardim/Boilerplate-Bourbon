
Boilerplate Bourbon + Neat + Bitter + Reffils + Jade
============

This project is my start project boilerplate based on [static-starter](https://github.com/crisberrios/static-starter/) which includes jade templating, HTML5 boilerplate, Normalize, html5shiv, [bourbon](http://www.bourbon.io), neat, bitters and reffils.

It also includes Velocity and jQuery 2.x (velocity dependency). You can easily remove them from package.json before installing.

### My modifications

What I did was create a simple layout for a home, about, news and contact page to get you started more easily. To the original [project](https://github.com/crisberrios/static-starter/) I've added several .scss, .sass and .jade files to build some common blocks based on Refills.

### Install npm dependencies
```
npm install
```

After that, just run the `default` gulp task with:
```
gulp
```

### Configuration
All paths and plugin settings have been abstracted into a centralized config object in `gulp/config.js`. Adapt the paths and settings to the structure and needs of your project.


#### Production files

There is also a `production` task you can run: 
```
gulp production
```
This will run JavaScript tests, then re-build optimized, compressed css and js files to the build folder, as well as output their file sizes to the console. It's a shortcut for running the following tasks: `karma`, `images`, `sass`,`pubfiles`, `jade`, `minifyCss`, `uglifyJs`.

#### JavaScript Tests with Karma
This repo includes a basic js testing setup with the following: [Karma](http://karma-runner.github.io/0.12/index.html), [Mocha](http://mochajs.org/), [Chai](http://chaijs.com/), and [Sinon](http://sinonjs.org/). There is `karma` gulp task, which the `production` task uses to run the tests before compiling. If any tests fail, the `production` task will abort.

To run the tests and start monitoring files:
```
./node_modules/karma/bin/karma start
```

Want to just run `karma start`? Either add `alias karma="./node_modules/karma/bin/karma"` to your shell config or install the karma command line interface globally with `npm install -g karma-cli`.

