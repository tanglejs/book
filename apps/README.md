# Apps

## What is an App?

An app is a
[single-page application](https://en.wikipedia.org/wiki/Single-page_application)
that implements...

* An "app-level" configuration scope.
* A [Marionette.Application](https://github.com/marionettejs/backbone.marionette/blob/master/docs/marionette.application.md)
* A layout template
* A base stylesheet
* Any number of initializers
* Any number of modules
* Integration tests

## What does it look like?

    .
    ├── index.coffee
    ├── index.jade
    ├── initializers
    │   ├── backbone.coffee
    │   └── logger.coffee
    ├── main.coffee
    ├── modules
    │   └── core
    ├── primitives
    ├── styl
    │   └── app.styl
    └── tangle.json
