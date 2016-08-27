#canvas
作用：展示绘图效果 画布   ie9+支持  不支持该标签  会当作div使用
基本语法：
1. 使用canvas标签,即可在页面中开辟一个区域，可以设置其宽高
2. 默认大小 宽：300px 高：150Px
3. 不能用css设置宽高，应该使用HTML属性
4. 如果浏览器不支持该标签，会将其解析为div标签；因此常常在canvas中嵌入文本，以提示用户浏览器的能力
5. canvas的兼容性非常强，只要支持该功能的都一样，因此不考虑兼容问题
6. canvas本身不能绘图，是使用javascript来完成绘图。canvas对象提供了各种绘图的api

canvas绘图:
1. 必须有canvas画布
2. 利用画布获得绘图工具
    * getContext('2d')         平面图
    * getContext('webgl')      立体图
    * 利用2d返回一个CanvasRenderingContext2D 类型的对象
3. render 渲染（刷新）
4. 绘图工具中提供一个方法 moveTo(x,y) 设置绘图的起点坐标
5. 绘图工具中提供一个方法 lineTo(x,y) 从当前位置绘制到哪里
6. 每次在调用绘图方法的时候，实际上在描点
7. 调用stroke将所有的点连起来，才能看到结果
8. 填充绘制：context.fill()
9. 闭合路径：context.closePath()

## canvas坐标系
###绘制连续的线段
1. 在绘图过程中会保留moveTo的位置到LineTo的位置，在保留当前位置到下一个lineTo的位置

结论：
1. 绘图要获得上下文，即绘图工具
2. 绘图需要设置开始的坐标
3. 绘图是先描点，然后一个一个依次连接
4. 依次绘图只能绘制单一样式

###填充：
fill()
如果描点的路径没有闭合，填充会自动将开始的点和最后一个点连接起来
context.fillStyle='';来设置填充的颜色







































