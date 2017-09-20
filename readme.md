# webpack-concat-svg-plugin
[![npm package](https://img.shields.io/npm/v/webpack-concat-svg-plugin.svg)](https://www.npmjs.org/package/webpack-concat-svg-plugin)


This plugin based on [webpack-concat-plugin](https://github.com/hxlniada/webpack-concat-plugin) and created to concat svg to one file

Plugin use [SVGO](https://github.com/svg/svgo) to minify svg content;

### Install
```
npm install webpack-concat-svg-plugin --save-dev
```

### Usage
```
const SvgConcatPlugin = require('webpack-concat-svg-plugin');

new SvgConcatPlugin({
    /**
    * If true using SVGO with default options;
    * If false not using SVGO;
    * Also you can pass SVGO options object;
    * @param Boolean|Object
    */
    svgo: true, 

    /**
    * Use hash in filename
    * @param Boolean
    */
    useHash: false,

    /**
    * Name of file
    * @param String
    */
    name: 'icons',

    /**
    * File name template 
    * @param String
    */
    fileName: '[name].[hash].svg',

    /**
    * List of files, which should be concatenated
    * @param Array<String>
    */
    filesToConcat:  ['./src/icons/play.svg', './src/icons/pause.svg']
});
```