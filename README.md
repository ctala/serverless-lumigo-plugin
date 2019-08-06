# serverless-lumigo

[![serverless](http://public.serverless.com/badges/v3.svg)](http://www.serverless.com)
[![version](https://badge.fury.io/js/serverless-lumigo.svg)](https://www.npmjs.com/package/serverless-lumigo)
[![License](https://img.shields.io/badge/License-Apache%202.0-blue.svg)](LICENSE)
[![codecov](https://codecov.io/gh/lumigo-io/serverless-lumigo/branch/master/graph/badge.svg?token=8mXE2G04ZO)](https://codecov.io/gh/lumigo-io/serverless-lumigo)

Serverless framework plugin to auto-install the Lumigo tracer for Node.js and Python functions.

## TOC

- [Install](#install)
- [Node.js functions](#nodejs-functions)

## Install

Run `npm install` in your Serverless project.

`$ npm install --save-dev serverless-lumigo`

Add the plugin to your serverless.yml file

```yml
plugins:
  - serverless-lumigo
```

## Node.js functions

For Node.js functions, the plugin would install the latest version of the Lumigo tracer for Node.js during `serverless package` and `serverless deploy`. It would also wrap your functions as well, so you only need to configure your Lumigo token in a `custom` section inside the `serverless.yml`.

For example:

```yml
provider:
  name: aws
  runtime: nodejs10.x

custom:
  lumigo:
    token: <YOUR TOKEN GOES HERE>
```

