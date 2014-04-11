# Plugins

## What is a Plugin?

A plugin implements a piece of Tangle functionality installed to your system
as a global **npm** module. There are several types of plugins, such as
**generator**, **runner**, and **scope**. A **scope** plugin may contain
both generators __and__ runners, under top-level subcommand.

## Design

Regardless of type, a plugin exposes the same functionality in exactly two
ways - through the JavaScript API, and through the shell command.

### Subcommands

A plugin must have a base command - though the base command can do nothing
but log usage instructions if desired.

A plugin may have any number of subcommands in addition to its base command,
and may accept an array of additional arguments.

### Subcommand function signature

The subcommand function must be resolveable by `require` at
`{module}/{subcommand}`, `{module}/{subcommand}/{subcommand}`, etc.

A subcommand function must accept an arguments object, and return a function
which accepts a final config object. This function should return a Q promise.

This promise may implement progress notifications if appropriate. When the task
is complete, the promise should be fulfilled with the logger and a data object.

### Arguments

All plugin commands must accept the following arguments:

    --cwd=""         Operate inside the specified working directory.
    --json           Return JSON-formatted output.
    --config=""      Accept a JSON-formatted config string.

JSON output (`--json`) defaults to `false` in shell usage, but defaults to
`true` in module usage.

```json
{
  "cwd": process.cwd(),
  "json": true,
  "config": undefined
}
```
