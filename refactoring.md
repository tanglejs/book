# Refactoring

As your project grows, you will begin to notice opportunities to refactor and
reuse the components you have created. To encourage this behavior, Tangle
provides intelligent tools to automate several common refactoring patterns.

## Extract module

Extract a module from your project into a new repository, preserving its
history, and install it instead as an external dependency.

    $ tangle module extract
    # ... interactive configuration

## Convert module to primitive

Convert a module implementation into a new primitive, and reimplement the module
extending from that primitive.

    $ tangle module primitive
    # ... interactive configuration

## Extract primitive

Extract a primitive from your project into a new repository, preserving its
history, and install it instead as an external dependency.

    $ tangle primitive extract
    # ... interactive configuration

## Reparent module

Create a new module and reparent several modules into it to group related
features together, or move a submodule up to an ancestor or into a different
group altogether.

    $ tangle module reparent
    # ... interactive configuration
