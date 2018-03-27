# tools

## 开发

```
// 启动服务器：接受Native拉取ZIP信息的HTTP请求，eg： "/" 打开二维码；"/bundle" 下载ZIP包；
npm run server
// 打包编译脚本文件到build目录；生成dist/zip文件；ZipPlugin插件向Native Server发送HTTP更新请求
npm run watch
// 如果仅更新一次脚本文件就编译，请使用下条；否则使用上条，持续watch
npm run debug
// 打包
npm run build
npm run release

// NA端的浏览器渲染环境
// 开发环境dv：watch模式
npm run na
// 开发环境dv：编译输出
npm run na:dv
// 测试环境qa：编译输出
npm run na:qa
// 线上环境ol：编译输出
npm run na:ol
```

## 常见问题

1. 查看webpack-dev-server都编译了哪些页面？

通过 http://localhost:8080/webpack-dev-server打开查看

2. 我的代码中需要区分(平台：na)或者(阶段: dv|qa|ol)，怎么办？

请参考当前目录下的webpack.config.js中的DefinePlugin的使用或者参考官网，在您的代码中if之类引用判断即可；JS压缩后会自动剔除掉无相关平台或者阶段的代码；


