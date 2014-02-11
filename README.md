sphere-coffeelint
=================

Coffeelint configuration file used in SPHERE.IO coffeescript projects.

## Setup

Add a dependency to github repo [sphere-coffeelint](https://github.com/sphereio/sphere-coffeelint) in your npm config (*package.json*).

```
  ...
  "devDependencies": {
    ...
    "sphere-coffeelint": "git://github.com/sphereio/sphere-coffeelint.git#master"
  }
  ..
```

Configure coffeelint to use the file *coffeelint.json* from module *sphere-coffeelint*.

```javascipt
  ...
  coffeelint:
    options: grunt.file.readJSON('node_modules/sphere-coffeelint/coffeelint.json')
    default: ["Gruntfile.coffee", "src/**/*.coffee"]
  ...
```
