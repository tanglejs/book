# Configuration

All configuration is stored in JSON format, in files managed by the
[tangle-config](https://github.com/tanglejs/config) **core plugin**.

## Cascading reads

Configuration cascades down from `$HOME/.tangle` to the working directory,
merging values from any file called `tangle.json`.

This enables awesome convenience and flexibility.

For example, you can set `user:email` to your personal address in the top-level
file `~/.tangle`, but keep your work projects under `~/work`, and add a
`~/work/tangle.json` file with `user:email` set to use your company address.

Finally, you can also pass the option `--config=[JSON_STRING]` to any command
to override the cascaded values.

## Global scope

> `$HOME/.tangle`, `**/tangle.json`

The **global scope** stores general user preferences that are not specific to a
plugin or context, such as your email address and Github username.

These values may be read by any plugin, but will not be included in the
`tangle.json` that is available to the browser once your project has been built.

When a plugin reads a global scope value that has not been set at any level,
you will be prompted, or in non-interactive mode, the process will terminate
with an error.

When any prompt starts to feel a bit repetitive, consider saving a global
scope value.
