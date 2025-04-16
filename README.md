# 天地图GeoJSON加载示例

这是一个简单的Web应用程序，展示如何在天地图上加载和显示GeoJSON数据。本示例使用火龙街道的边界数据。

## 使用方法

1. 获取天地图API密钥
   - 访问[天地图开发者平台](https://console.tianditu.gov.cn/api/key)注册并获取API密钥
   - 在`index.html`文件中替换所有`YOUR_TIANDITU_KEY`为你获取的密钥

2. 运行应用
   - 双击`index.html`文件在浏览器中打开，或
   - 使用Web服务器托管这些文件（推荐）

## 功能特点

- 使用天地图的矢量底图和注记图层
- 加载并显示火龙街道边界GeoJSON数据
- 自动缩放地图以适应GeoJSON数据范围
- 图层控制面板，可以切换显示/隐藏图层

## 文件说明

- `index.html`: 主要的HTML文件，包含地图初始化和GeoJSON加载的代码
- `火龙街道_shape.json`: 包含火龙街道边界数据的GeoJSON文件

## 技术栈

- Leaflet.js: 开源JavaScript地图库
- 天地图API: 中国国家地理信息公共服务平台

## 注意事项

- 天地图API密钥有每日请求次数限制，请合理使用
- 建议通过Web服务器访问，避免跨域问题
- 如需使用更多天地图图层，请参考[天地图开发文档](https://lbs.tianditu.gov.cn/api/js4.0/guide.html)

## 自定义样式

可以通过修改`index.html`中的GeoJSON样式参数来自定义边界显示：

```javascript
style: {
    color: '#ff0000',     // 边界线颜色
    weight: 2,            // 边界线宽度
    opacity: 1,           // 边界线透明度
    fillColor: '#ff7800', // 填充颜色
    fillOpacity: 0.2      // 填充透明度
}
``` 