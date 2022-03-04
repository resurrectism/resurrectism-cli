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
$ npm install -g resurrectism-cli
$ resurrectism COMMAND
running command...
$ resurrectism (--version)
resurrectism-cli/0.0.0 darwin-x64 node-v16.13.0
$ resurrectism --help [COMMAND]
USAGE
  $ resurrectism COMMAND
...
```
<!-- usagestop -->
# Commands
<!-- commands -->
* [`resurrectism hello PERSON`](#resurrectism-hello-person)
* [`resurrectism hello world`](#resurrectism-hello-world)
* [`resurrectism help [COMMAND]`](#resurrectism-help-command)
* [`resurrectism plugins`](#resurrectism-plugins)
* [`resurrectism plugins:inspect PLUGIN...`](#resurrectism-pluginsinspect-plugin)
* [`resurrectism plugins:install PLUGIN...`](#resurrectism-pluginsinstall-plugin)
* [`resurrectism plugins:link PLUGIN`](#resurrectism-pluginslink-plugin)
* [`resurrectism plugins:uninstall PLUGIN...`](#resurrectism-pluginsuninstall-plugin)
* [`resurrectism plugins update`](#resurrectism-plugins-update)

## `resurrectism hello PERSON`

Say hello

```
USAGE
  $ resurrectism hello [PERSON] -f <value>

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

_See code: [dist/commands/hello/index.ts](https://github.com/resurrectism/resurrectism-cli/blob/v0.0.0/dist/commands/hello/index.ts)_

## `resurrectism hello world`

Say hello world

```
USAGE
  $ resurrectism hello world

DESCRIPTION
  Say hello world

EXAMPLES
  $ oex hello world
  hello world! (./src/commands/hello/world.ts)
```

## `resurrectism help [COMMAND]`

Display help for resurrectism.

```
USAGE
  $ resurrectism help [COMMAND] [-n]

ARGUMENTS
  COMMAND  Command to show help for.

FLAGS
  -n, --nested-commands  Include all nested commands in the output.

DESCRIPTION
  Display help for resurrectism.
```

_See code: [@oclif/plugin-help](https://github.com/oclif/plugin-help/blob/v5.1.10/src/commands/help.ts)_

## `resurrectism plugins`

List installed plugins.

```
USAGE
  $ resurrectism plugins [--core]

FLAGS
  --core  Show core plugins.

DESCRIPTION
  List installed plugins.

EXAMPLES
  $ resurrectism plugins
```

_See code: [@oclif/plugin-plugins](https://github.com/oclif/plugin-plugins/blob/v2.0.11/src/commands/plugins/index.ts)_

## `resurrectism plugins:inspect PLUGIN...`

Displays installation properties of a plugin.

```
USAGE
  $ resurrectism plugins:inspect PLUGIN...

ARGUMENTS
  PLUGIN  [default: .] Plugin to inspect.

FLAGS
  -h, --help     Show CLI help.
  -v, --verbose

DESCRIPTION
  Displays installation properties of a plugin.

EXAMPLES
  $ resurrectism plugins:inspect myplugin
```

## `resurrectism plugins:install PLUGIN...`

Installs a plugin into the CLI.

```
USAGE
  $ resurrectism plugins:install PLUGIN...

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
  $ resurrectism plugins add

EXAMPLES
  $ resurrectism plugins:install myplugin 

  $ resurrectism plugins:install https://github.com/someuser/someplugin

  $ resurrectism plugins:install someuser/someplugin
```

## `resurrectism plugins:link PLUGIN`

Links a plugin into the CLI for development.

```
USAGE
  $ resurrectism plugins:link PLUGIN

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
  $ resurrectism plugins:link myplugin
```

## `resurrectism plugins:uninstall PLUGIN...`

Removes a plugin from the CLI.

```
USAGE
  $ resurrectism plugins:uninstall PLUGIN...

ARGUMENTS
  PLUGIN  plugin to uninstall

FLAGS
  -h, --help     Show CLI help.
  -v, --verbose

DESCRIPTION
  Removes a plugin from the CLI.

ALIASES
  $ resurrectism plugins unlink
  $ resurrectism plugins remove
```

## `resurrectism plugins update`

Update installed plugins.

```
USAGE
  $ resurrectism plugins update [-h] [-v]

FLAGS
  -h, --help     Show CLI help.
  -v, --verbose

DESCRIPTION
  Update installed plugins.
```
<!-- commandsstop -->
# resurrectism-cli
