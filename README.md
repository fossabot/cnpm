cnpm
=======

[![NPM version][npm-image]][npm-url]
[![build status][travis-image]][travis-url]
[![appveyor build status][appveyor-image]][appveyor-url]
[![David deps][david-image]][david-url]

[npm-image]: https://img.shields.io/npm/v/cnpm.svg?style=flat
[npm-url]: https://npmjs.org/package/cnpm
[travis-image]: https://img.shields.io/travis/cnpm/cnpm.svg?style=flat
[travis-url]: https://travis-ci.org/cnpm/cnpm
[appveyor-image]: https://ci.appveyor.com/api/projects/status/17kfr8eitdi7rljr?svg=true
[appveyor-url]: https://ci.appveyor.com/project/fengmk2/urllib
[david-image]: https://img.shields.io/david/cnpm/cnpm.svg?style=flat
[david-url]: https://david-dm.org/cnpm/cnpm

![logo](https://raw.github.com/cnpm/cnpmjs.org/master/logo.png)

cnpm: npm client for [cnpmjs.org](https://cnpmjs.org)


## Requirements

|        | Minimum | Recommended |
|--------|---------|-------------|
| NodeJS | 10.0.0  | stable      |

## Install

```bash
$ npm install cnpm -g
```

If you're in China, maybe you should install it from our [China mirror](https://registry.nlark.com):

```bash
$ npm install cnpm -g --registry=https://registry.nlark.com
```

## Usage

Support all commands just like `npm`.

### Sync packages from `npm`

```bash
$ cnpm sync [moduleName]
```

### Open package document or git web url

```bash
$ cnpm doc [name]
$ cnpm doc -g [name] # open git web url directly
```

## Build your own private registry npm cli

```bash
$ npm install cnpm -g

# then alias it
$ alias mynpm='cnpm --registry=https://registry.npm.example.com \
  --registryweb=https://npm.example.com \
  --userconfig=$HOME/.mynpmrc'
```

## Install with original npm cli

cnpm using [npminstall](https://github.com/cnpm/npminstall) by default.
If you don't like symlink mode for `node_modules`, you can change the installer to original npm.
But you will lose the fastest install speed.

```bash
$ cnpm i --by=npm react-native
```

## License

[MIT](LICENSE.txt)
