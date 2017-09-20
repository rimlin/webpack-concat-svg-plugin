# webpack-concat-svg-plugin
[![npm package](https://img.shields.io/npm/v/webpack-concat-svg-plugin.svg)](https://www.npmjs.org/package/webpack-concat-svg-plugin)
[![npm downloads](http://img.shields.io/npm/dm/webpack-concat-svg-plugin.svg)](https://www.npmjs.org/package/webpack-concat-svg-plugin)

This plugin based on [webpack-concat-plugin](https://github.com/hxlniada/webpack-concat-plugin) and created to concat svg to one file

### Install
```
npm install webpack-concat-svg-plugin --save-dev
```

### Usage
```
const ConcatPlugin = require('webpack-concat-svg-plugin');

new ConcatPlugin({
    uglify: true, // or you can set uglifyjs options
    useHash: true, // md5 file
    sourceMap: true, // generate sourceMap
    name: 'flexible', // used in html-webpack-plugin
    fileName: '[name].[hash].bundle.js', // would output to 'flexible.d41d8cd98f00b204e980.bundle.js'
    filesToConcat: ['./src/lib/flexible.js', './src/lib/makegrid.js']
});

