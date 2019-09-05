### Canvas 
uni Canvas插件基于[GCanvas](https://github.com/alibaba/GCanvas)实现了微信小程序[CanvasContext API](https://developers.weixin.qq.com/miniprogram/dev/api/canvas/CanvasContext.html),  W3C [WebGL API](https://developer.mozilla.org/en-US/docs/Web/API/WebGL_API)
该工程为uni Canvas插件使用演示demo

### 使用
1. 将gcanvas目录复制到HBX uniapp 工程下
2. 在页面中引入canvas js
```javascript
import {
	enable,
	WeexBridge
} from '[自己的路径]/gcanvas/index.js';
```
3. 获取Canvas context
```javascript
 /*通过元素引用获取canvas对象*/
 var ganvas = this.$refs["gcanvess"];
 var canvasObj = enable(ganvas, {bridge: WeexBridge});
 /*获取绘图所需的上下文*/
 var context = canvasObj.getContext('2d');
 var gl = canvasObj.getContext("webgl");
 /*调用具体API*/
```
## API支持情况
* Canvas API
API|Status|
:-|:-|
createOffscreenCanvas|❌
canvasToTempFilePath|✅
canvasPutImageData|✅
canvasGetImageData|✅
createImage|✅
requestAnimationFrame|❌
CanvasGradient|✅
Color|✅
Image|✅
OffscreenCanvas|❌
* CanvasContext API
API|Status|
:-|:-|
arc|✅
arcTo|✅
beginPath|✅	
bezierCurveTo|✅	
clearRect|✅
clip|✅
closePath|✅
createCircularGradient|✅
createLinearGradient|✅
createPattern|❌
draw|✅
drawImage|✅	
fill|✅
fillRect|✅
fillText|✅
lineTo|✅
measureText|✅
moveTo|✅
quadraticCurveTo|✅
rect|✅
restore|✅
rotate|✅
save|✅
scale|✅
setFillStyle|✅
setFontSize|✅
setGlobalAlpha|✅
setLineCap|✅
setLineDash|❌
setLineJoin|✅
setLineWidth|✅
setMiterLimit|✅
setShadow| ❌
setStrokeStyle|✅
setTextAlign|✅
setTextBaseline|✅
setTransform|✅
stroke|✅
strokeRect|✅
strokeText|✅
transform|✅
translate|✅
* WebGL请参考[https://alibaba.github.io/GCanvas/docs/WebGL.html](https://alibaba.github.io/GCanvas/docs/WebGL.html)
