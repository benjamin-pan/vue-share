# vue-share

> vue components for share.js

一键分享到微博、QQ空间、QQ好友、微信、腾讯微博、豆瓣、Facebook、Twitter、Linkedin、Google+、点点等社交网站。
已经封装成vue组件，修复IE浏览器不显示微信分享二维码bug。

# 安装

有多种安装方式：

1. 使用 [npm](https://npmjs.com)

    ```shell
    npm install share-for-vue
    ```
2. 手动下载或者 git clone 本项目。

# 引用

```js
import Share from '_share-for-vue@1.0.6@share-for-vue'
import '_share-for-vue@1.0.6@share-for-vue/src/css/share.min.css'
Vue.use(Share)
```

# 使用

HTML:

```html
<share :config="config"></share>
```

## 自定义配置

所有配置**可选**， 通常默认就满足需求：

可用的配置有：

```js

url                 : '', // 网址，默认使用 window.location.href
source              : '', // 来源（QQ空间会用到）, 默认读取head标签：<meta name="site" content="http://overtrue" />
title               : '', // 标题，默认读取 document.title 或者 <meta name="title" content="share.js" />
origin          : '', // 分享 @ 相关 twitter 账号
description       : '', // 描述, 默认读取head标签：<meta name="description" content="PHP弱类型的实现原理分析" />
image               : '', // 图片, 默认取网页中第一个img标签
sites               : ['qzone', 'qq', 'weibo','wechat', 'douban'], // 启用的站点
disabled            : ['google', 'facebook', 'twitter'], // 禁用的站点
wechatQrcodeTitle   : '微信扫一扫：分享', // 微信二维码提示文字
wechatQrcodeHelper  : '<p>微信里点“发现”，扫一下</p><p>二维码便可将本文分享至朋友圈。</p>'
```

示例代码：

```js
config: {
    title               : '这里是标题',
    description         : '这里是描述',
    wechatQrcodeTitle   : "微信扫一扫：分享", // 微信二维码提示文字
    wechatQrcodeHelper  : '<p>微信里点“发现”，扫一下</p><p>二维码便可将本文分享至朋友圈。</p>',
};
```

# 引用

本项目中二维码生成部分用到了开源组件：[lrsjng/jquery-qrcode](https://github.com/lrsjng/jquery-qrcode) (MIT License)

# License

 MIT
For detailed explanation on how things work, consult the [docs for vue-loader](http://vuejs.github.io/vue-loader).
