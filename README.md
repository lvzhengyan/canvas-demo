# canvas-demo

使用canvas绘制一个简单的画板，实现 PC 按下鼠标绘制线条，手机端触摸绘制线条


用JavaScript来画线会非常卡顿，会一直创建 DOM 节点，用 canvas 就会快很多

```
// 判断是否支持触控
var isTouchDevice = 'ontouchstart' in document.documentElement;
```

```
// 用来绘制线条，从(x1,y1)到(x2,y2)
function drawLine(x1, y1, x2, y2) {
    ctx.beginPath();
    ctx.moveTo(x1, y1);
    ctx.lineTo(x2, y2);
    ctx.stroke();
}
```