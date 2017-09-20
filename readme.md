# webpack-concat-svg-plugin
[![npm package](https://img.shields.io/npm/v/webpack-concat-svg-plugin.svg)](https://www.npmjs.org/package/webpack-concat-svg-plugin)


This plugin based on [webpack-concat-plugin](https://github.com/hxlniada/webpack-concat-plugin) and created to concat svg to one file

### Install
```
npm install webpack-concat-svg-plugin --save-dev
```

### Usage
```
const SvgConcatPlugin = require('webpack-concat-svg-plugin');

new SvgConcatPlugin({
    minify: true,
    useHash: false,
    sourceMap: false,
    name: 'icons',
    fileName: '[name].svg',
    filesToConcat:  ['./src/icons/play.svg', './src/icons/pause.svg']
});
```