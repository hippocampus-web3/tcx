oclif-hello-world
=================

oclif example Hello World CLI

[![oclif](https://img.shields.io/badge/cli-oclif-brightgreen.svg)](https://oclif.io)
[![CircleCI](https://circleci.com/gh/oclif/hello-world/tree/main.svg?style=shield)](https://circleci.com/gh/oclif/hello-world/tree/main)
[![GitHub license](https://img.shields.io/github/license/oclif/hello-world)](https://github.com/oclif/hello-world/blob/main/LICENSE)

<!-- toc -->
* [Usage](#usage)
* [Commands](#commands)
<!-- tocstop -->
# Usage
<!-- usage -->
```sh-session
$ npm install -g mirin
$ mirin COMMAND
running command...
$ mirin (--version)
mirin/0.0.0 darwin-arm64 node-v18.17.1
$ mirin --help [COMMAND]
USAGE
  $ mirin COMMAND
...
```
<!-- usagestop -->
# Commands
<!-- commands -->
* [`mirin hello PERSON`](#mirin-hello-person)
* [`mirin hello world`](#mirin-hello-world)
* [`mirin help [COMMANDS]`](#mirin-help-commands)
* [`mirin plugins`](#mirin-plugins)
* [`mirin plugins:install PLUGIN...`](#mirin-pluginsinstall-plugin)
* [`mirin plugins:inspect PLUGIN...`](#mirin-pluginsinspect-plugin)
* [`mirin plugins:install PLUGIN...`](#mirin-pluginsinstall-plugin-1)
* [`mirin plugins:link PLUGIN`](#mirin-pluginslink-plugin)
* [`mirin plugins:uninstall PLUGIN...`](#mirin-pluginsuninstall-plugin)
* [`mirin plugins:uninstall PLUGIN...`](#mirin-pluginsuninstall-plugin-1)
* [`mirin plugins:uninstall PLUGIN...`](#mirin-pluginsuninstall-plugin-2)
* [`mirin plugins update`](#mirin-plugins-update)

## `mirin hello PERSON`

Say hello

```
USAGE
  $ mirin hello PERSON -f <value>

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

## `mirin hello world`

Say hello world

```
USAGE
  $ mirin hello world

DESCRIPTION
  Say hello world

EXAMPLES
  $ mirin hello world
  hello world! (./src/commands/hello/world.ts)
```

## `mirin help [COMMANDS]`

Display help for mirin.

```
USAGE
  $ mirin help [COMMANDS] [-n]

ARGUMENTS
  COMMANDS  Command to show help for.

FLAGS
  -n, --nested-commands  Include all nested commands in the output.

DESCRIPTION
  Display help for mirin.
```

_See code: [@oclif/plugin-help](https://github.com/oclif/plugin-help/blob/v5.2.20/src/commands/help.ts)_

## `mirin plugins`

List installed plugins.

```
USAGE
  $ mirin plugins [--json] [--core]

FLAGS
  --core  Show core plugins.

GLOBAL FLAGS
  --json  Format output as json.

DESCRIPTION
  List installed plugins.

EXAMPLES
  $ mirin plugins
```

_See code: [@oclif/plugin-plugins](https://github.com/oclif/plugin-plugins/blob/v3.8.4/src/commands/plugins/index.ts)_

## `mirin plugins:install PLUGIN...`

Installs a plugin into the CLI.

```
USAGE
  $ mirin plugins:install PLUGIN...

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
  $ mirin plugins add

EXAMPLES
  $ mirin plugins:install myplugin

  $ mirin plugins:install https://github.com/someuser/someplugin

  $ mirin plugins:install someuser/someplugin
```

## `mirin plugins:inspect PLUGIN...`

Displays installation properties of a plugin.

```
USAGE
  $ mirin plugins:inspect PLUGIN...

ARGUMENTS
  PLUGIN  [default: .] Plugin to inspect.

FLAGS
  -h, --help     Show CLI help.
  -v, --verbose

GLOBAL FLAGS
  --json  Format output as json.

DESCRIPTION
  Displays installation properties of a plugin.

EXAMPLES
  $ mirin plugins:inspect myplugin
```

_See code: [@oclif/plugin-plugins](https://github.com/oclif/plugin-plugins/blob/v3.8.4/src/commands/plugins/inspect.ts)_

## `mirin plugins:install PLUGIN...`

Installs a plugin into the CLI.

```
USAGE
  $ mirin plugins:install PLUGIN...

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
  $ mirin plugins add

EXAMPLES
  $ mirin plugins:install myplugin

  $ mirin plugins:install https://github.com/someuser/someplugin

  $ mirin plugins:install someuser/someplugin
```

_See code: [@oclif/plugin-plugins](https://github.com/oclif/plugin-plugins/blob/v3.8.4/src/commands/plugins/install.ts)_

## `mirin plugins:link PLUGIN`

Links a plugin into the CLI for development.

```
USAGE
  $ mirin plugins:link PLUGIN

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
  $ mirin plugins:link myplugin
```

_See code: [@oclif/plugin-plugins](https://github.com/oclif/plugin-plugins/blob/v3.8.4/src/commands/plugins/link.ts)_

## `mirin plugins:uninstall PLUGIN...`

Removes a plugin from the CLI.

```
USAGE
  $ mirin plugins:uninstall PLUGIN...

ARGUMENTS
  PLUGIN  plugin to uninstall

FLAGS
  -h, --help     Show CLI help.
  -v, --verbose

DESCRIPTION
  Removes a plugin from the CLI.

ALIASES
  $ mirin plugins unlink
  $ mirin plugins remove
```

## `mirin plugins:uninstall PLUGIN...`

Removes a plugin from the CLI.

```
USAGE
  $ mirin plugins:uninstall PLUGIN...

ARGUMENTS
  PLUGIN  plugin to uninstall

FLAGS
  -h, --help     Show CLI help.
  -v, --verbose

DESCRIPTION
  Removes a plugin from the CLI.

ALIASES
  $ mirin plugins unlink
  $ mirin plugins remove
```

_See code: [@oclif/plugin-plugins](https://github.com/oclif/plugin-plugins/blob/v3.8.4/src/commands/plugins/uninstall.ts)_

## `mirin plugins:uninstall PLUGIN...`

Removes a plugin from the CLI.

```
USAGE
  $ mirin plugins:uninstall PLUGIN...

ARGUMENTS
  PLUGIN  plugin to uninstall

FLAGS
  -h, --help     Show CLI help.
  -v, --verbose

DESCRIPTION
  Removes a plugin from the CLI.

ALIASES
  $ mirin plugins unlink
  $ mirin plugins remove
```

## `mirin plugins update`

Update installed plugins.

```
USAGE
  $ mirin plugins update [-h] [-v]

FLAGS
  -h, --help     Show CLI help.
  -v, --verbose

DESCRIPTION
  Update installed plugins.
```

_See code: [@oclif/plugin-plugins](https://github.com/oclif/plugin-plugins/blob/v3.8.4/src/commands/plugins/update.ts)_
<!-- commandsstop -->
