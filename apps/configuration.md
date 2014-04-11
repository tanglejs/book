# App configuration

## App scope

> `yourProject/apps/yourApp/tangle.json`

The **app scope** configuration file contains app metadata, custom options
specific to the project environment, and a map of initializers and modules to
be loaded when the app is started.

It also serves as a marker to indicate that this directory is the root of a
Tangle app.

These values may be read by any plugin, and will also be included in the
`tangle.json` that is available to the running app once your project has been
built.
