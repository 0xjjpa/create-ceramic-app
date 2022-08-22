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
$ npm install -g create-ceramic
$ create-ceramic COMMAND
running command...
$ create-ceramic (--version)
create-ceramic/0.0.0 darwin-arm64 node-v16.4.2
$ create-ceramic --help [COMMAND]
USAGE
  $ create-ceramic COMMAND
...
```
<!-- usagestop -->
# Commands
<!-- commands -->
* [`create-ceramic hello PERSON`](#create-ceramic-hello-person)
* [`create-ceramic hello world`](#create-ceramic-hello-world)
* [`create-ceramic help [COMMAND]`](#create-ceramic-help-command)
* [`create-ceramic plugins`](#create-ceramic-plugins)
* [`create-ceramic plugins:install PLUGIN...`](#create-ceramic-pluginsinstall-plugin)
* [`create-ceramic plugins:inspect PLUGIN...`](#create-ceramic-pluginsinspect-plugin)
* [`create-ceramic plugins:install PLUGIN...`](#create-ceramic-pluginsinstall-plugin-1)
* [`create-ceramic plugins:link PLUGIN`](#create-ceramic-pluginslink-plugin)
* [`create-ceramic plugins:uninstall PLUGIN...`](#create-ceramic-pluginsuninstall-plugin)
* [`create-ceramic plugins:uninstall PLUGIN...`](#create-ceramic-pluginsuninstall-plugin-1)
* [`create-ceramic plugins:uninstall PLUGIN...`](#create-ceramic-pluginsuninstall-plugin-2)
* [`create-ceramic plugins update`](#create-ceramic-plugins-update)

## `create-ceramic hello PERSON`

Say hello

```
USAGE
  $ create-ceramic hello [PERSON] -f <value>

ARGUMENTS
  PERSON  Person to say hello to

FLAGS
  -f, --from=<value>  (required) Whom is saying hello

DESCRIPTION
  Say hello

EXAMPLES
  $ oex hello friend --from oclif
  hello friend from oclif! (./src/commands/hello/index.ts)
```

_See code: [dist/commands/hello/index.ts](https://github.com/Sterahi/hello-world/blob/v0.0.0/dist/commands/hello/index.ts)_

## `create-ceramic hello world`

Say hello world

```
USAGE
  $ create-ceramic hello world

DESCRIPTION
  Say hello world

EXAMPLES
  $ oex hello world
  hello world! (./src/commands/hello/world.ts)
```

## `create-ceramic help [COMMAND]`

Display help for create-ceramic.

```
USAGE
  $ create-ceramic help [COMMAND] [-n]

ARGUMENTS
  COMMAND  Command to show help for.

FLAGS
  -n, --nested-commands  Include all nested commands in the output.

DESCRIPTION
  Display help for create-ceramic.
```

_See code: [@oclif/plugin-help](https://github.com/oclif/plugin-help/blob/v5.1.10/src/commands/help.ts)_

## `create-ceramic plugins`

List installed plugins.

```
USAGE
  $ create-ceramic plugins [--core]

FLAGS
  --core  Show core plugins.

DESCRIPTION
  List installed plugins.

EXAMPLES
  $ create-ceramic plugins
```

_See code: [@oclif/plugin-plugins](https://github.com/oclif/plugin-plugins/blob/v2.0.11/src/commands/plugins/index.ts)_

## `create-ceramic plugins:install PLUGIN...`

Installs a plugin into the CLI.

```
USAGE
  $ create-ceramic plugins:install PLUGIN...

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
  $ create-ceramic plugins add

EXAMPLES
  $ create-ceramic plugins:install myplugin 

  $ create-ceramic plugins:install https://github.com/someuser/someplugin

  $ create-ceramic plugins:install someuser/someplugin
```

## `create-ceramic plugins:inspect PLUGIN...`

Displays installation properties of a plugin.

```
USAGE
  $ create-ceramic plugins:inspect PLUGIN...

ARGUMENTS
  PLUGIN  [default: .] Plugin to inspect.

FLAGS
  -h, --help     Show CLI help.
  -v, --verbose

DESCRIPTION
  Displays installation properties of a plugin.

EXAMPLES
  $ create-ceramic plugins:inspect myplugin
```

## `create-ceramic plugins:install PLUGIN...`

Installs a plugin into the CLI.

```
USAGE
  $ create-ceramic plugins:install PLUGIN...

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
  $ create-ceramic plugins add

EXAMPLES
  $ create-ceramic plugins:install myplugin 

  $ create-ceramic plugins:install https://github.com/someuser/someplugin

  $ create-ceramic plugins:install someuser/someplugin
```

## `create-ceramic plugins:link PLUGIN`

Links a plugin into the CLI for development.

```
USAGE
  $ create-ceramic plugins:link PLUGIN

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
  $ create-ceramic plugins:link myplugin
```

## `create-ceramic plugins:uninstall PLUGIN...`

Removes a plugin from the CLI.

```
USAGE
  $ create-ceramic plugins:uninstall PLUGIN...

ARGUMENTS
  PLUGIN  plugin to uninstall

FLAGS
  -h, --help     Show CLI help.
  -v, --verbose

DESCRIPTION
  Removes a plugin from the CLI.

ALIASES
  $ create-ceramic plugins unlink
  $ create-ceramic plugins remove
```

## `create-ceramic plugins:uninstall PLUGIN...`

Removes a plugin from the CLI.

```
USAGE
  $ create-ceramic plugins:uninstall PLUGIN...

ARGUMENTS
  PLUGIN  plugin to uninstall

FLAGS
  -h, --help     Show CLI help.
  -v, --verbose

DESCRIPTION
  Removes a plugin from the CLI.

ALIASES
  $ create-ceramic plugins unlink
  $ create-ceramic plugins remove
```

## `create-ceramic plugins:uninstall PLUGIN...`

Removes a plugin from the CLI.

```
USAGE
  $ create-ceramic plugins:uninstall PLUGIN...

ARGUMENTS
  PLUGIN  plugin to uninstall

FLAGS
  -h, --help     Show CLI help.
  -v, --verbose

DESCRIPTION
  Removes a plugin from the CLI.

ALIASES
  $ create-ceramic plugins unlink
  $ create-ceramic plugins remove
```

## `create-ceramic plugins update`

Update installed plugins.

```
USAGE
  $ create-ceramic plugins update [-h] [-v]

FLAGS
  -h, --help     Show CLI help.
  -v, --verbose

DESCRIPTION
  Update installed plugins.
```
<!-- commandsstop -->