# HTML常用标签

## 1.a 标签的用法

```
herf="url"   跳转        //#id/tel:/mailto:   id锚点/打电话/发邮件 
target=""    窗口        //_b/_t/_p   新开/顶窗开/父窗开(用于嵌套)
target=""    传递url     //iframe的name值
href="javascript:;"  点击不刷新(不推荐)
```



## 2.img 标签的用法

```
src="url"     图片        //get请求
alt=""        请求失败文本
w/h=""        宽/高       //一边会等比缩放
max-width="100%"  响应式  //重点
```



## 3.table 标签的用法

```
table>thead+tbody+tfoot     //表格>表头+表内容+表脚
tr>th+td                    //一行表格>标题+内容
----
align=""           table对齐   //左/右/中
table-layout:      table布局   //fixed
border-collapse:   table合并   //collapse
border-spacing:    table间距   //px
border:            th/td边框   //1px solid 颜色
----
table无宽高, 2种布局都使用单元格之和
table有宽高, auto固定总宽高, flxed选最优
```



## 4.其他感想

暂时没有

