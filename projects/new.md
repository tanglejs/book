# Creating a new project

The [tangle-project](https://github.com/tanglejs/project) **core plugin**
includes a generator to help you get started.

## Basic usage

### Interactive

```bash
$ mkdir blog
$ cd blog
$ tangle project new
# ... interactive configuration
```

### Non-interactive

```bash
$ mkdir blog
$ cd blog
$ tangle project new --config=$(cat projectConfig.json)
# ... interactive configuration
```

### From a script

```coffeescript
generator = require 'tangle-project/new'

generator(process.cwd).run
  name: 'blog'
  version: '0.0.0'
.progress (event) ->
  console.log event
.then (result) ->
  console.log 'Project generated'
.fail (err) ->
  throw new Error 'An error occurred'
```

## Need help?

Try `$ man tangle-project-new` and `$ tangle help project new`

