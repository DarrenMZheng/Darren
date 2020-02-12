# nwjs编写浏览器外壳
某些展示性的网站，例如地铁用于路线指引的网站、社区办理大厅的流程指引网站，都需要浏览器全屏展示（F11）。使用浏览器全屏会有以下弊端：
- 页面跳转左下角会显示跳转地址
- 点击页面会出现鼠标点
- 闪屏

之前了解过`node-webkit`,现在改成`nwjs`,所以使用`nwjs`编写浏览器全屏外壳，`nwjs`的优点在这里就不重复了，有兴趣可以访问[官网](https://nwjs.io/)。

## 配置文件说明
```
nwjs/
│   ├── src            
│   │   ├── config.js    // 配置           
│   │   ├── index.html   // 入口html
│   │   ├── logo.jpg     // logo
│   ├── package.json     // 主要配置入口页面
```

### config.js
配置需要跳转的页面地址
```
{
	"url":"http://www.baidu.com/"
}
```

### index.html
主要控制页面跳转、快捷键监听、退出等功能。

## 使用说明
- 配置src/config.js 里的url
- 双击打开nw.exe，程序自动会加载config配置的url
- 退出确认快捷键`Ctrl+Shift+D`,点击确认即可退出
