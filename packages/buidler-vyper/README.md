# buidler-example-plugin

[![npm](https://img.shields.io/npm/v/@nomiclabs/buidler-vyper.svg)](https://www.npmjs.com/package/@nomiclabs/buidler-vyper)

[Buidler](http://getbuidler.com) plugin example to develop smart contracts with Vyper.

## What

This plugin adds support for Vyper to Buidler. Once installed, Vyper contracts will be compile by the `compile` task.

This plugin generates teh same artifact format than the Solidity contracts' one, so it can be used in conjunction with
all the rest of the plugins.

The Vyper compiler is run using the [official Docker images](https://hub.docker.com/r/ethereum/vyper).

## Installation

First, you have to install Docker Desktop by following its [Get Started guide](https://www.docker.com/get-started).

Then, you need to install the plugin by running

```bash
npm install @nomiclabs/buidler-vyper
```

And add the following statement to your `buidler.config.js`:

```js
usePlugin("@nomiclabs/buidler-vyper");
```

## Required plugins

No plugin is required to use this one.

## Tasks

This plugin creates no additional tasks.

## Environment extensions

This plugin does not extend the Buidler Runtime Environment.

## Configuration

This plugin adds an optional `vyper` entry to Buidler's config, which lets you specify the Vyper version to use. If no
version is given, the [latest one on Docker Hub](https://hub.docker.com/r/ethereum/vyper/tags) will be used.

This is an example of how to set it:

```js
module.exports = {
  vyper: {
    version: "0.1.0b9"
  }
};
```

## Usage

There are no additional steps you need to take for this plugin to work.

## TypeScript support

You need to add this to your `tsconfig.json`'s `files` array:
`"node_modules/@nomiclabs/buidler-vyper/src/type-extensions.d.ts"`