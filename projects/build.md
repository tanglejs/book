# Building projects

## Cleaning the build directory

`$ tangle build clean`

This will completely empty the `build/` directory.

## Building the entire project

`$ tangle build`

Building a project compiles all of its apps, style guides, and API docs to a
tree under `build/apps/`, optimized and configured for the
[active environment](/project/environments.html).

## Rebuilding a single component

Read `$ tangle help build tasks` to see what components can be updated without
completely rebuilding the project.

## Watching files for changes

Building a large project can take a while, so while you're developing it is
better to rebuild only the components that have actually changed.

Fortunately, the [tangle-watch](https://github.com/tanglejs/watch) plugin will
take care of that, and also update your browser if you happen to be viewing the
component that changed.

`$ tangle watch`

