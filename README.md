##安装nodejs和cordova
npm install -g cordova.
##创建cordova
cordova create cordova-app
cordova platform add browser
cordova platform list
cordova run browser

##创建cordova 桌面版本

cordova create cordova-electron
cordova platform add electron
cordova platform list
cordova run browser
cordova build electron --release


## 添加 vue


npm install -g @vue/cli
vue  init  webpack  vueapp


build\utils.js

    if (options.extract) {
      return ExtractTextPlugin.extract({
        publicPath: '../', //添加此行
        use: loaders,
        fallback: 'vue-style-loader'
      })


config/index.js

  build: {

    index: path.resolve(__dirname, '../../www/index.html'),
    assetsRoot: path.resolve(__dirname, '../../www'),
    assetsSubDirectory: 'static',
    assetsPublicPath: '', //此处修改