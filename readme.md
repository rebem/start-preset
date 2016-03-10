# start-rebem-preset

[![npm](https://img.shields.io/npm/v/start-rebem-preset.svg?style=flat-square)](https://www.npmjs.com/package/start-rebem-preset)
[![travis](http://img.shields.io/travis/rebem/start-preset.svg?style=flat-square)](https://travis-ci.org/rebem/start-preset)
[![deps](https://img.shields.io/gemnasium/rebem/start-preset.svg?style=flat-square)](https://gemnasium.com/rebem/start-preset)
[![gitter](https://img.shields.io/badge/gitter-join_chat_%E2%86%92-46bc99.svg?style=flat-square)](https://gitter.im/rebem/rebem)

[Start](https://github.com/start-runner/start) preset for [reBEM](https://github.com/rebem/rebem).

## Install

```
npm i -D start-rebem-preset
```

## Usage

See [documentation](https://github.com/start-runner/start#readme) and [source tasks file](lib/index.js) for details.

### Simple

```js
// package.json
"devDependencies": {
  "start-babel-cli": "0.x.x",
  "start-rebem-preset": "0.x.x"
},
"scripts": {
  "start": "start-runner start-rebem-preset"
}
```

Available commands:

```
npm start build
npm start dev
npm start lint
npm start test
npm start tdd
npm start coverage
npm start ci
```

### Extend

```js
// tasks.js
import start from 'start-rebem-preset';

export * from 'start-rebem-preset';

export function myTasksRunner() {
    return start(
        ...
    );
}
```

<sup>* example is rely on [babel-plugin-transform-export-extensions](https://babeljs.io/docs/plugins/transform-export-extensions/) from [babel-preset-stage-1](https://babeljs.io/docs/plugins/preset-stage-1/)</sup>

```js
// package.json
"devDependencies": {
  "start-babel-cli": "0.x.x",
  "start-rebem-preset": "0.x.x"
},
"scripts": {
  "start": "start-runner ./tasks"
}
```

Available commands:

```
npm start build
npm start dev
npm start lint
npm start test
npm start tdd
npm start coverage
npm start ci
npm start myTasksRunner
```
