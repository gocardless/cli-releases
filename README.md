# Gocardless CLI

The Gocardless CLI enables you to build and test your Gocardless integration right from the terminal.

**A brief outline of things you can do with the CLI:**

- Trigger events directly from terminal and test webhooks 
- Transition payment objects from one state to another
- Create, retrieve, update, or delete API objects.

## Installation

Gocardless CLI is available for macOS, Windows, and Linux for distros like Ubuntu, Debian, RedHat and CentOS.

Refer to the [getting started page] (https://developer.gocardless.com/getting-started/developer-tools/gocardless-cli/) for more on how to get started

### macOS

Gocardless CLI is available on macOS via [Homebrew](https://brew.sh/):

```sh
brew install gocardless/taps/cli
```

### Linux

Refer to the [installation instructions](https://developer.gocardless.com/cli-reference#installation) for available Linux installation options.

### Windows

Refer to the [installation instructions](https://developer.gocardless.com/cli-reference#installation) for available Windows installation options.

### Docker

The GC CLI is also available as a [Docker image](https://hub.docker.com/r/gocardless/gc-cli).

First set up a volume for the gc-cli container:

```sh
docker volume create gc_config
```

To login

```sh
docker run -v gc_config:/.gc-cli -p 8080:8080 --rm -it gocardless/gc-cli:latest login
```

To run commands

```sh
docker run -v gc_config:/.gc-cli --rm -it gocardless/gc-cli:latest [command]
```

## Usage

Once installed, you now have access to the `gc` command.

```sh-session
gc [command]

# Run `--help` for detailed information about CLI commands
gc [command] help
```

## Commands

The Gocardless CLI supports a broad range of commands. Below is some of the most used ones:
- [`login`](https://developer.gocardless.com/cli-reference/gc_login/)
- [`listen`](https://developer.gocardless.com/cli-reference/gc_listen/)
- [`trigger`](https://developer.gocardless.com/cli-reference/gc_trigger/)
- [`list`](https://developer.gocardless.com/cli-reference/gc_list/)
- [`get`](https://developer.gocardless.com/cli-reference/gc_get/)
- [`config`](https://developer.gocardless.com/cli-reference/gc_config/)
- [`open`](https://developer.gocardless.com/cli-reference/gc_open/)
- [`create`](https://developer.gocardless.com/cli-reference/gc_create/)

## Documentation

For a full reference, see the [CLI reference site](https://developer.gocardless-staging.io/cli-reference)

## Feedback

For any feedback you might have for us, please open an issue within the repository.

## License
Copyright (c) Gocardless. All rights reserved.

Licensed under the [Apache License 2.0 license](LICENSE).
