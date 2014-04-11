# Projects

## What is a Project?

A project is a directory that houses one or more **apps**, along with various
dependencies and files associated with those apps, and a "project-level"
configuration scope.

In the most simple case, a project contains a single app, defined inside it,
with barebones configuration and no dependencies apart from the handful required
by Tangle itself.

In a more complex scenario, a project might include several apps as external
dependencies, such as a blog engine and admin panel, and configure them to
implement the complete website.

## What does it look like?

    .
    ├── apps
    ├── bower_components
    │   ├── backbone
    │   ├── backbone.babysitter
    │   ├── backbone.marionette
    │   ├── backbone.wreqr
    │   ├── loglevel
    │   ├── require-jade
    │   ├── requirejs
    │   ├── requirejs-plugins
    │   └── underscore
    ├── bower.json
    ├── build
    │   └── apps
    ├── config.js
    ├── node_modules
    │   ├── coffee-script
    │   └── loglevel
    ├── package.json
    └── tangle.json
