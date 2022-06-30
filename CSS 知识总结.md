## 浏览器渲染原理

渲染过程: 构建dom树, 构建css树, 合并树, 布局(位置/大小), 绘制(颜色/阴影), 合成

更新方式: js, 样式, 布局, 绘制, 合成  (布局/绘制可能省略)

使用浏览器rendering的画面闪烁, 可以查看重绘次数, 越少性能越好



## css 动画

* transition: all 1s       过渡 (属性名/耗时)      //一次性动画 (配合hover/js)

* animation: @key名 1s   动画 (动画函数/耗时)     //分段循环动画 (配合key)
  * @key 名{ 0%{...} 100%{...} }        动画函数         //所有阶段的变化
  * 其余参数:  ease曲线  0s延迟  1/inf次数  alter反向  for结束暂停

曲线:  linear匀速、ease慢快慢、e-in变快、e-out变慢、e-i-o慢平慢、steps(10)步长




## css 变换
```
transf: translX(px/%)、transl(x,y)、transl3d(x,y,z)    变换-位移 (单/双/三轴)
transf: rotateX(90deg)、rotate(90deg)                  变换-旋转 (单轴/平面)
transf: scaleX(1.5)、scale(1.5)                        变换-缩放 (单轴/平面)
transf: skewX(45deg)                                   变换-倾斜 (单轴)
psp: 1000px                     透视点 (先辈加)         //作用于 "位移z轴 / 旋转xy轴"
tran-style: preserve-3d         3d空间 (父加)           //作用于 "旋转嵌套旋转"
backface-visibility: hid        隐藏旋转后的背面
```
