# Creating a new app

The [tangle-app](https://github.com/tanglejs/app) **core plugin** includes a
generator to help you get started.

## Demonstration

<script
  type="text/javascript"
  src="https://asciinema.org/a/8801.js"
  id="asciicast-8801"
  data-speed="2"
  data-size="small"
  data-autoplay="1" async></script>

## Basic usage

### Interactive

```bash
$ cd myproject
$ tangle app new
# ... interactive configuration
```

### Non-interactive

```bash
$ cd myproject
$ tangle app new --config=$(cat appConfig.json)
# ... interactive configuration
```

### From a script

```coffeescript
generator = require 'tangle-app/new'

generator(process.cwd).run
  name: 'blog'
  version: '0.0.0'
.progress (event) ->
  console.log event
.then (result) ->
  console.log 'App generated'
.fail (err) ->
  throw new Error 'An error occurred'
```

## Need help?

Try `$ man tangle-app-new` and `$ tangle help app new`

