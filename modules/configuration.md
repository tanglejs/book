# Module configuration

## Module scope

> `yourProject/apps/yourApp/modules/yourModule/tangle.json`

The **module scope** configuration file contains module metadata, custom
options specific to the project environment, and a map of initializers and
routes to be loaded when the app is started.

It also serves as a marker to indicate that this directory is the root of a
Tangle module.

These values may be read by any plugin, and will also be included in the
`tangle.json` that is available to the running module once your project has
been built.
