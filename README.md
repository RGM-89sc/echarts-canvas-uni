# echarts-canvas-uni

## 来源

代码根据 [echarts-for-weixin](https://github.com/ecomfe/echarts-for-weixin) 项目进行修改。

注意：

* wx API改为使用uni-app API，支持APP。
* 由于使用了uni-app的canvas API，放弃使用微信小程序基础库2.9.0所支持的新版canvas API，原来的forceUseOldCanvas参数已无效。
* `echarts.js`可自行替换为最新版本的echarts，或者使用官方[自定义构建](https://echarts.apache.org/zh/builder.html)生成

## 使用

使用方式：

```vue
<echarts-canvas-uni canvas-id="mychart" :ec="ec"></echarts-canvas-uni>
```

ec参数数据结构：

```typescript
interface IEc {
  initConfig: {
    options: EChartOption
  }
  lazyLoad: boolean
  disableTouch: boolean
}
```

echarts options详见[官方文档](https://echarts.apache.org/zh/option.html)

## 其他问题

如果使用了[echarts-for-weixin](https://github.com/ecomfe/echarts-for-weixin)项目中的`echarts.js`，在APP中可能会出现 [Vue warn]: Error in event handler for "view.onRequestComponentInfo": "TypeError: Cannot read property 'type' of null" 导致无法运行，重新下载echart即可，[传送门](https://echarts.apache.org/zh/download.html)
