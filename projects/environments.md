# Environments

A project has three environments:

* **development** (default)
* **test**
* **production**

Many tasks are optimized differently for each environment. Builds are created
in a per-environment subdirectory of `yourProject/builds`.

Additionally, if your apps contain environment-scoped configuration objects,
the active environment at build-time will determine which configuration object
is used at runtime.

## Active Environment

Any time you trigger a build, you do so in the context of the **active
environment**. This is persisted in the
[project config](/projects/configuration.html) file, and can be switched there
or overridden using the standard `--config=[JSON_STRING]` argument.

For convenience, the
[tangle-environment](https://github.com/tanglejs/environment) **core plugin**
is included

#### Echo the active environment
    $ tangle environment
      # => development

#### Switch the active environment
    $ tangle environment [development|test|production]

You may find it convenient to add the active environment to your shell prompt.
