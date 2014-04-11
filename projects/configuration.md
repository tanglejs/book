# Project configuration

> `yourProject/tangle.json`

The **project scope** configuration file contains project metadata and active
state such as the current environment.

It also serves as a marker to indicate that this directory is the root of a
Tangle project.

These values may be read by any plugin, but will not be included in the
`tangle.json` that is available to the browser once your project has been built.

## Example

```json
{
  "name": "exampleProject",
  "type": "project",
  "version": "0.0.0",
  "environment": "development",
  "apps": {
    "exampleApp": "apps/exampleApp"
  }
}
```
