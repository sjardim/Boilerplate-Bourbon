
Boilerplate Bourbon + Neat + Bitter + Reffils + Jade
============

This project is my start project boilerplate based on [static-starter](https://github.com/crisberrios/static-starter/) which includes jade templating, HTML5 boilerplate, Normalize, html5shiv, [bourbon](http://www.bourbon.io), neat, bitters and reffils.

### My modifications

What I did was create a simple layout for a home, about, news and contact page to get you started more easily. To the original [project](https://github.com/crisberrios/static-starter/) I've added several .scss, .sass and .jade files to build some common blocks based on Refills.

I also rebuild Refill navigation snippet into a **flexbox version**. I didn't like the use of JQuery for the mobile menu. I provided the Photoshop CS6 files for the hero image and the background. The bar logo I borrowed from codyhouse.co and the cards images are from Flickr.

**Feel free create issues, fork it and send pull requests**.

## DEMO

### [http://sjardim.github.io/Boilerplate-Bourbon/](http://sjardim.github.io/Boilerplate-Bourbon/)

![](https://raw.githubusercontent.com/sjardim/Boilerplate-Bourbon/master/preview.png)


### To Do
 - Fallback for the flexbox menu for old IEs
 - Test on Windows browsers
 - Test on mobile hardware

---
Original doc:

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

## License

MIT