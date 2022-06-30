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





https://shimo.im/docs/aBAYVErJnJiyaR3j/ 《前端----饥人谷》，可复制链接后用石墨文档 App 或小程序打开

