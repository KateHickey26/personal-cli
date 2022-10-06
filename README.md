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
$ npm install -g personal-cli
$ personal-cli COMMAND
running command...
$ personal-cli (--version)
personal-cli/0.0.0 darwin-x64 node-v16.5.0
$ personal-cli --help [COMMAND]
USAGE
  $ personal-cli COMMAND
...
```
<!-- usagestop -->
# Commands
<!-- commands -->
* [`personal-cli hello PERSON`](#personal-cli-hello-person)
* [`personal-cli hello world`](#personal-cli-hello-world)
* [`personal-cli help [COMMAND]`](#personal-cli-help-command)
* [`personal-cli plugins`](#personal-cli-plugins)
* [`personal-cli plugins:install PLUGIN...`](#personal-cli-pluginsinstall-plugin)
* [`personal-cli plugins:inspect PLUGIN...`](#personal-cli-pluginsinspect-plugin)
* [`personal-cli plugins:install PLUGIN...`](#personal-cli-pluginsinstall-plugin-1)
* [`personal-cli plugins:link PLUGIN`](#personal-cli-pluginslink-plugin)
* [`personal-cli plugins:uninstall PLUGIN...`](#personal-cli-pluginsuninstall-plugin)
* [`personal-cli plugins:uninstall PLUGIN...`](#personal-cli-pluginsuninstall-plugin-1)
* [`personal-cli plugins:uninstall PLUGIN...`](#personal-cli-pluginsuninstall-plugin-2)
* [`personal-cli plugins update`](#personal-cli-plugins-update)

## `personal-cli hello PERSON`

Say hello

```
USAGE
  $ personal-cli hello [PERSON] -f <value>

ARGUMENTS
  PERSON  Person to say hello to

FLAGS
  -f, --from=<value>  (required) Who is saying hello

DESCRIPTION
  Say hello

EXAMPLES
  $ oex hello friend --from oclif
  hello friend from oclif! (./src/commands/hello/index.ts)
```

_See code: [dist/commands/hello/index.ts](https://github.com/KateHickey26/personal-cli/blob/v0.0.0/dist/commands/hello/index.ts)_

## `personal-cli hello world`

Say hello world

```
USAGE
  $ personal-cli hello world

DESCRIPTION
  Say hello world

EXAMPLES
  $ personal-cli hello world
  hello world! (./src/commands/hello/world.ts)
```

## `personal-cli help [COMMAND]`

Display help for personal-cli.

```
USAGE
  $ personal-cli help [COMMAND] [-n]

ARGUMENTS
  COMMAND  Command to show help for.

FLAGS
  -n, --nested-commands  Include all nested commands in the output.

DESCRIPTION
  Display help for personal-cli.
```

_See code: [@oclif/plugin-help](https://github.com/oclif/plugin-help/blob/v5.1.14/src/commands/help.ts)_

## `personal-cli plugins`

List installed plugins.

```
USAGE
  $ personal-cli plugins [--core]

FLAGS
  --core  Show core plugins.

DESCRIPTION
  List installed plugins.

EXAMPLES
  $ personal-cli plugins
```

_See code: [@oclif/plugin-plugins](https://github.com/oclif/plugin-plugins/blob/v2.1.1/src/commands/plugins/index.ts)_

## `personal-cli plugins:install PLUGIN...`

Installs a plugin into the CLI.

```
USAGE
  $ personal-cli plugins:install PLUGIN...

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
  $ personal-cli plugins add

EXAMPLES
  $ personal-cli plugins:install myplugin 

  $ personal-cli plugins:install https://github.com/someuser/someplugin

  $ personal-cli plugins:install someuser/someplugin
```

## `personal-cli plugins:inspect PLUGIN...`

Displays installation properties of a plugin.

```
USAGE
  $ personal-cli plugins:inspect PLUGIN...

ARGUMENTS
  PLUGIN  [default: .] Plugin to inspect.

FLAGS
  -h, --help     Show CLI help.
  -v, --verbose

DESCRIPTION
  Displays installation properties of a plugin.

EXAMPLES
  $ personal-cli plugins:inspect myplugin
```

## `personal-cli plugins:install PLUGIN...`

Installs a plugin into the CLI.

```
USAGE
  $ personal-cli plugins:install PLUGIN...

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
  $ personal-cli plugins add

EXAMPLES
  $ personal-cli plugins:install myplugin 

  $ personal-cli plugins:install https://github.com/someuser/someplugin

  $ personal-cli plugins:install someuser/someplugin
```

## `personal-cli plugins:link PLUGIN`

Links a plugin into the CLI for development.

```
USAGE
  $ personal-cli plugins:link PLUGIN

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
  $ personal-cli plugins:link myplugin
```

## `personal-cli plugins:uninstall PLUGIN...`

Removes a plugin from the CLI.

```
USAGE
  $ personal-cli plugins:uninstall PLUGIN...

ARGUMENTS
  PLUGIN  plugin to uninstall

FLAGS
  -h, --help     Show CLI help.
  -v, --verbose

DESCRIPTION
  Removes a plugin from the CLI.

ALIASES
  $ personal-cli plugins unlink
  $ personal-cli plugins remove
```

## `personal-cli plugins:uninstall PLUGIN...`

Removes a plugin from the CLI.

```
USAGE
  $ personal-cli plugins:uninstall PLUGIN...

ARGUMENTS
  PLUGIN  plugin to uninstall

FLAGS
  -h, --help     Show CLI help.
  -v, --verbose

DESCRIPTION
  Removes a plugin from the CLI.

ALIASES
  $ personal-cli plugins unlink
  $ personal-cli plugins remove
```

## `personal-cli plugins:uninstall PLUGIN...`

Removes a plugin from the CLI.

```
USAGE
  $ personal-cli plugins:uninstall PLUGIN...

ARGUMENTS
  PLUGIN  plugin to uninstall

FLAGS
  -h, --help     Show CLI help.
  -v, --verbose

DESCRIPTION
  Removes a plugin from the CLI.

ALIASES
  $ personal-cli plugins unlink
  $ personal-cli plugins remove
```

## `personal-cli plugins update`

Update installed plugins.

```
USAGE
  $ personal-cli plugins update [-h] [-v]

FLAGS
  -h, --help     Show CLI help.
  -v, --verbose

DESCRIPTION
  Update installed plugins.
```
<!-- commandsstop -->
