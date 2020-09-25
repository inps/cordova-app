## 安装nodejs和cordova
npm install -g cordova.
## 创建cordova
cordova create cordova-app
cordova platform add browser
cordova platform list
cordova run browser

## 创建cordova 桌面版本

cordova create cordova-electron
cordova platform add electron
cordova platform list
cordova run browser
cordova build electron --release


## 开发，先安装Android studio ， 配置android_home_root , java_home环境变量。

$ cordova platform add android
该命令将在platforms目录下，自动生成android平台的工程。
也可以用以下命令删除已添加的平台工程：
$ cordova platform remove android
以下命令查看添加了哪些平台：
$ cordova platform list
编译工程
以下命令编译cordova工程：
$ cordova build
也可以单独编译一个平台的工程：
$ cordova build android
 运行工程
在android平台，以下命令运行模拟器：
$ cordova emulate android
模拟器运行后，以下命令测试工程：
$ cordova run android




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