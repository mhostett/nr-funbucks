oclif-hello-world
=================

oclif example Hello World CLI

[![oclif](https://img.shields.io/badge/cli-oclif-brightgreen.svg)](https://oclif.io)
[![Version](https://img.shields.io/npm/v/oclif-hello-world.svg)](https://npmjs.org/package/oclif-hello-world)
[![CircleCI](https://circleci.com/gh/oclif/hello-world/tree/main.svg?style=shield)](https://circleci.com/gh/oclif/hello-world/tree/main)
[![Downloads/week](https://img.shields.io/npm/dw/oclif-hello-world.svg)](https://npmjs.org/package/oclif-hello-world)
[![License](https://img.shields.io/npm/l/oclif-hello-world.svg)](https://github.com/oclif/hello-world/blob/main/package.json)

<!-- toc -->
* [Usage](#usage)
* [Commands](#commands)
<!-- tocstop -->
# Usage
<!-- usage -->
```sh-session
$ npm install -g nr-funbucks
$ nr-funbucks COMMAND
running command...
$ nr-funbucks (--version)
nr-funbucks/1.0.0 darwin-x64 node-v17.3.1
$ nr-funbucks --help [COMMAND]
USAGE
  $ nr-funbucks COMMAND
...
```
<!-- usagestop -->
# Commands
<!-- commands -->
* [`nr-funbucks gen`](#nr-funbucks-gen)
* [`nr-funbucks help [COMMAND]`](#nr-funbucks-help-command)
* [`nr-funbucks plugins`](#nr-funbucks-plugins)
* [`nr-funbucks plugins:inspect PLUGIN...`](#nr-funbucks-pluginsinspect-plugin)
* [`nr-funbucks plugins:install PLUGIN...`](#nr-funbucks-pluginsinstall-plugin)
* [`nr-funbucks plugins:link PLUGIN`](#nr-funbucks-pluginslink-plugin)
* [`nr-funbucks plugins:uninstall PLUGIN...`](#nr-funbucks-pluginsuninstall-plugin)
* [`nr-funbucks plugins update`](#nr-funbucks-plugins-update)

## `nr-funbucks gen`

generate fluentbit configuration

```
USAGE
  $ nr-funbucks gen [-n <value>]

FLAGS
  -n, --name=<value>  name to print

DESCRIPTION
  generate fluentbit configuration

EXAMPLES
  $ nr-funbucks gen
```

_See code: [dist/commands/gen.ts](https://github.com/mbystedt/hello-world/blob/v1.0.0/dist/commands/gen.ts)_

## `nr-funbucks help [COMMAND]`

Display help for nr-funbucks.

```
USAGE
  $ nr-funbucks help [COMMAND] [-n]

ARGUMENTS
  COMMAND  Command to show help for.

FLAGS
  -n, --nested-commands  Include all nested commands in the output.

DESCRIPTION
  Display help for nr-funbucks.
```

_See code: [@oclif/plugin-help](https://github.com/oclif/plugin-help/blob/v5.1.11/src/commands/help.ts)_

## `nr-funbucks plugins`

List installed plugins.

```
USAGE
  $ nr-funbucks plugins [--core]

FLAGS
  --core  Show core plugins.

DESCRIPTION
  List installed plugins.

EXAMPLES
  $ nr-funbucks plugins
```

_See code: [@oclif/plugin-plugins](https://github.com/oclif/plugin-plugins/blob/v2.0.11/src/commands/plugins/index.ts)_

## `nr-funbucks plugins:inspect PLUGIN...`

Displays installation properties of a plugin.

```
USAGE
  $ nr-funbucks plugins:inspect PLUGIN...

ARGUMENTS
  PLUGIN  [default: .] Plugin to inspect.

FLAGS
  -h, --help     Show CLI help.
  -v, --verbose

DESCRIPTION
  Displays installation properties of a plugin.

EXAMPLES
  $ nr-funbucks plugins:inspect myplugin
```

## `nr-funbucks plugins:install PLUGIN...`

Installs a plugin into the CLI.

```
USAGE
  $ nr-funbucks plugins:install PLUGIN...

ARGUMENTS
  PLUGIN  Plugin to install.

FLAGS
  -f, --force    Run yarn install with force flag.
  -h, --help     Show CLI help.
  -v, --verbose

DESCRIPTION
  Installs a plugin into the CLI.

  Can be installed from npm or a git url.

  Installation of a user-installed plugin will override a core plugin.

  e.g. If you have a core plugin that has a 'hello' command, installing a user-installed plugin with a 'hello' command
  will override the core plugin implementation. This is useful if a user needs to update core plugin functionality in
  the CLI without the need to patch and update the whole CLI.

ALIASES
  $ nr-funbucks plugins add

EXAMPLES
  $ nr-funbucks plugins:install myplugin 

  $ nr-funbucks plugins:install https://github.com/someuser/someplugin

  $ nr-funbucks plugins:install someuser/someplugin
```

## `nr-funbucks plugins:link PLUGIN`

Links a plugin into the CLI for development.

```
USAGE
  $ nr-funbucks plugins:link PLUGIN

ARGUMENTS
  PATH  [default: .] path to plugin

FLAGS
  -h, --help     Show CLI help.
  -v, --verbose

DESCRIPTION
  Links a plugin into the CLI for development.

  Installation of a linked plugin will override a user-installed or core plugin.

  e.g. If you have a user-installed or core plugin that has a 'hello' command, installing a linked plugin with a 'hello'
  command will override the user-installed or core plugin implementation. This is useful for development work.

EXAMPLES
  $ nr-funbucks plugins:link myplugin
```

## `nr-funbucks plugins:uninstall PLUGIN...`

Removes a plugin from the CLI.

```
USAGE
  $ nr-funbucks plugins:uninstall PLUGIN...

ARGUMENTS
  PLUGIN  plugin to uninstall

FLAGS
  -h, --help     Show CLI help.
  -v, --verbose

DESCRIPTION
  Removes a plugin from the CLI.

ALIASES
  $ nr-funbucks plugins unlink
  $ nr-funbucks plugins remove
```

## `nr-funbucks plugins update`

Update installed plugins.

```
USAGE
  $ nr-funbucks plugins update [-h] [-v]

FLAGS
  -h, --help     Show CLI help.
  -v, --verbose

DESCRIPTION
  Update installed plugins.
```
<!-- commandsstop -->
