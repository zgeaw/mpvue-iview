# mpvue-iview

一套高质量的微信小程序 UI 组件库，支持Vue写法，支持Less，支持字体库，使小程序开发更加方便快捷


# 1、下载代码

``` 
git clone https://github.com/zgeaw/mpvue-iview.git
``` 

# 2、安装依赖

```
npm install 或者 cnpm i
```

# 3、开发时构建

```
npm dev

打开微信开发者工具，新建项目，将目录指向 /dist 即可实时预览效果

已全局引入iview-weapp，可直接使用

已全局引入Less，可直接写Less语法

```

# 4、打包构建

```
npm build
```

# 5、指定平台的开发时构建(微信、百度、头条、支付宝)

```
npm dev:wx
npm dev:swan
npm dev:tt
npm dev:my
```

# 6、指定平台的打包构建

```
npm build:wx
npm build:swan
npm build:tt
npm build:my
```

# 7、生成 bundle 分析报告

```
npm run build --report
```


For detailed explanation on how things work, checkout the [guide](http://vuejs-templates.github.io/webpack/) and [docs for vue-loader](http://vuejs.github.io/vue-loader).
