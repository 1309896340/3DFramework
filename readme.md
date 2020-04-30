# 已实现

## Stage 属性列表

biasX , biasY    用于将原点偏移指屏幕中央

tx , ty , tz    用于将坐标系进行旋转

tmr    由`setInterval()`返回的ID，可用于停止绘制



## Stage 方法列表

`transCdnt(x0,y0,z0)`    将三维坐标映射为屏幕二维坐标，返回值为Array对象

`drawCoordinate()`    绘制坐标轴，并显示坐标系的相关信息

`drawLine(x0,y0,z0,x1,y1,z1)`    绘制线段，内部会调用`transCdnt()`进行坐标映射

`drawCube(x,y,z,wx,wy,wz,style)`    在坐标 (x,y,z) 绘制长宽高 (wx,wy,wz) 样式为 style 的立方块线条

`run()`    启动一个计时器定时刷新画面

`stop()`    停止绘制



## 注册的Canvas事件

mousedown , mouseup , mousemove

主要用来实现鼠标拖动改变视角



## 其他事件

window.onresize    用于适应浏览器缩放

canvas.oncontextmenu    用于禁用右键菜单



# 待改进

1. 右击拖动改变视角，不能很好地控制
2. 能绘制的形体不够多样
3. 应将`run()`方法中绘图的具体细节分离出来，做成接口
4. `drawCube()`绘制立方块的写法太过粗暴

