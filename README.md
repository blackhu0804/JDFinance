## Vue京东金融组件化实践

这个项目使用的是`Vue.js`实现京东金融手机端的Web项目，着重使用了CSS模块化以及JS模块化，CSS模块化使用`Sass`组织代码，实现最大的模块化。

## 使用`CSS scoped`缺点

- 如果用户在别处定义了相同的类名，也许还是会影响到组件的样式
- 根据css样式优先级的特性，scoped这种处理会造成每个样式的权重加重了，如果要修改，需要更高的权重
- 会影响子组件的根节点样式
- scoped会使标签选择器渲染变慢很多倍

所以我们使用`CSS Modules`来完成CSS模块化和组合CSS，可以避免一个子组件的根节点会同时受其父组件的 `scoped CSS` 和子组件的 `scoped CSS` 的影响，并且标签选择器不会受影响。

## 移动端适配

通过`hotcss.js` 和 `px2rem-loader` 来实现通过只写 px 利用 `webpack` 来进行转换，通过这样的方式，只需要一套代码，就可以实现多终端自适应，而css数值可以与设计稿保持一致。

## 代码构建

构建部分使用 `Webpack` 和 `npm scripts`独立完成，不使用第三方脚手架。

## 预览地址：
[点击预览](http://www.blackhu.site/JDFinance/dist/index.html#/)

手机可直接预览，PC使用调试工具，切换至移动端调试预览

## 安装

```bash
git clone git@github.com:hu970804/JDFinance.git
npm install
npm start
```
