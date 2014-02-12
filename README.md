sphere-coffeelint
=================

Hosted coffeelint configuration file used in all SPHERE.IO coffeescript projects. To use the hosted *coffeelint.json* in another node project, make sure to follow given steps.

## Setup

* Add a module dependency to github repo [sphere-coffeelint](https://github.com/sphereio/sphere-coffeelint) in your npm config (*package.json*).

            ...
            "devDependencies": {
              ...
              "sphere-coffeelint": "git://github.com/sphereio/sphere-coffeelint.git#master"
            }
            ...

* update project dependencies (npm downloads the newly added *sphere-coffeelint* module to *node_modules/*)

            npm install

* Configure coffeelint in *Gruntfile.coffee* to use the file *coffeelint.json* located in the *sphere-coffeelint* module.

            ...
            coffeelint:
              options: grunt.file.readJSON('node_modules/sphere-coffeelint/coffeelint.json')
              default: ["Gruntfile.coffee", "src/**/*.coffee"]
            ...
