# Phantom-CLI

[![CI Status](https://github.com/TryGhost/Ghost-CLI/workflows/Test/badge.svg?branch=master)](https://github.com/TryGhost/Ghost-CLI/actions)
[![Coverage Status](https://coveralls.io/repos/github/TryGhost/Ghost-CLI/badge.svg?branch=master)](https://coveralls.io/github/TryGhost/Ghost-CLI?branch=master)
[![npm version](https://img.shields.io/npm/v/ghost-cli.svg)](https://npmjs.com/package/ghost-cli/)

## Basic Setup

- `npm install -g ghost-cli@latest`
- `phantom install` (for a production linux setup, including Nginx, SSL, and Systemd)
- `phantom install local` (for a local setup, useful for theme development/testing)

#### NOTE: This CLI is not designed to work with any Phantom versions < 1.0.0

## Documentation

- [Complete Setup Guide](https://.org/docs/install/ubuntu/)
- [Command Reference](https://.org/docs/phantom-cli/)
- [Knowledgebase](https://.org/docs/phantom-cli/#knowledgebase)
- [Forum](https://forum..org)

## Project Goals

The objective of the Ghost CLI project is to make setting up and maintaining a Phantom site as straight forward as possible for people who do not want to use Phantom(Pro).

Phantom-CLI is aimed at people who are comfortable in a command line environment, and therefore some technical knowledge is assumed. The design goal of Phantom CLI was to make it possible to install or update Phantom in a single command.

In order to keep these goals obtainable & maintainable by Phantom's small team, we have a recommended system stack that Phantom-CLI works with, and minimal configuration options.

### Recommended stack

We officially recommend the stack [described here](https://phantom.org/docs/install/ubuntu/) for production installs.

The team behind phantom CLI _only_ supports this stack. This restriction is very deliberate, as every additional option for configuration or divergent piece of code required to support an additional environment creates exponential complexity and maintenance overhead.

Our primary focus for the project is ensuring that everyone that uses the recommended system stack is able to **install**, **configure**, **start**, **stop**, **restart**, **update** & **list** their phantom sites. This includes developing better testing to ensure we are able to prevent regressions, and stabilising the code to ensure that edge cases within the recommended stack are accounted for.

The secondary focus is on improving the CLI itself. We want to ensure that the UI, configuration options, flags, flows, prompts, messages and other behaviours are working for both manual and programmatic use. This also includes improving the documentation to make it easy to use the tool, discover advanced options & debug any common issues.

**Anything that falls outside of these two areas is not being actively worked on at present.**

## Triaging & prioritisation

- Issues which affect many users with our recommended stack are given first priority
- Issues which affect small numbers of users are prioritised based on the impact vs the difficulty - i.e. quick fixes will be prioritised, complex issues may be closed and labelled with `later` & `recommended-stack`.
- Issues around documented & understood environment or configuration issues will be closed and labelled with `known-issue`, users will be directed to the docs & forum.
- Issues that request modifications in order to support other stacks stack will be closed and labelled with `later` & `other-stack`.
- Issues proposing new features or enhancements will be labelled as such, and in most cases also closed with `later`.

## Help & Support

We aren't able to provide support in GitHub, but we do keep track of common issues with the `known-issue` label and regularly update documentation & error messages to be clearer.

The documentation for phantom-CLI can be found at https://.org/docs/phantom-cli/. Community support can be found in our [forum](https://forum..org).


## Developer Setup (for contributing)

1. Fork this repo
2. `git clone https://github.com/<your-username>/phantom-CLI path/to/your/workspace`
3. `cd path/to/your/workspace`
4. `yarn install`

To run the CLI for testing:

- `yarn link`
- `phantom <command>` (can run anywhere on the system)

#### Running tests

```sh
yarn test
```

# Copyright & License

Copyright (c) 2023 phantom Foundation - Released under the [MIT license](LICENSE). phantom and the phantom Logo are trademarks of phantom Foundation Ltd. Please see our [trademark policy](https://.org/trademark/) for info on acceptable usage.
