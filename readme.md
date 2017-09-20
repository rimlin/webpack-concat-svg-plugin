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

### Inject inline SVG content to html
To inject inline svg content in output html page you need to use [html-webpack-plugin](https://github.com/jantimon/html-webpack-plugin).
Your svg content is stored in `htmlWebpackPlugin.files.webpackConcatSvg[name]` variable, where `[name]` is your name of file.

Example of usage:

*index.ejs*
```
    ...

    <div style="height: 0;">
      <%= htmlWebpackPlugin.files.webpackConcatSvg.icons %>
    </div>
  </body>
</html>
```