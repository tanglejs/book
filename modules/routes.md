# Routes

## Module routing

Modules that implement routing should do so with a single [Marionette.Controller](https://github.com/marionettejs/backbone.marionette/blob/master/docs/marionette.controller.md)
and [Marionette.AppRouter](https://github.com/marionettejs/backbone.marionette/blob/master/docs/marionette.approuter.md)
, with a routes object loaded from the **module scope** configuration (`config.routes`).
