## jQuery 如何获取元素

~~~
　　$(document)             //选择整个文档对象
　　$('#myId')              //选择ID为myId的网页元素
　　$('div.myClass')        //选择class为myClass的div元素
　　$('input[name=first]')  //选择name属性等于first的input元素
　　$('a:first')            //选择网页中第一个a元素
　　$('tr:odd')             //选择表格的奇数行
　　$('#myForm :input')     //选择表单中的input元素
　　$('div:visible')        //选择可见的div元素
　　$('div:gt(2)')          //选择所有的div元素，除了前三个
　　$('div:animated')       //选择当前处于动画状态的div元素
　　$('div').has('p');      //选择包含p元素的div元素
　　$('div').first();       //选择第1个div元素
　　$('div').eq(5);         //选择第6个div元素
　　$('div').not('.myClass');    //选择class不等于myClass的div元素
　　$('div').filter('.myClass'); //选择class等于myClass的div元素
　　$('div').next('p');       //选择div元素后面的第一个p元素
　　$('div').parent();        //选择div元素的父元素
　　$('div').closest('form'); //选择离div最近的那个form父元素
　　$('div').children();      //选择div的所有子元素
　　$('div').siblings();      //选择div的同级元素
~~~



## jQuery 的链式操作是怎样的

```
　$('div').find('h3').eq(2).html('Hello');
　----
 $('div')        //找到div元素
  .find('h3')     //选择其中的h3元素
  .eq(2)          //选择第3个h3元素
  .html('Hello'); //将它的内容改为Hello
```



## jQuery 如何创建元素

~~~
　$('<p>Hello</p>');                     //创建p元素
　$('ul').append('<li>list item</li>');  //在ul里面追加li元素
~~~

 

## jQuery 如何移动元素

~~~
　$('div').insertAfter($('p'));    //把div元素移动p元素后面, 返回div
　$('p').after($('div'));          //把p元素加到div元素前面, 返回p
---
.insertAfter()和.after()        //在现存元素的外部，从后面插入元素    插在兄弟后面
.insertBefore()和.before()      //在现存元素的外部，从前面插入元素    插在兄弟前面
.appendTo()和.append()          //在现存元素的内部，从后面插入元素     
.prependTo()和.prepend()        //在现存元素的内部，从前面插入元素
~~~



## jQuery 如何修改元素的属性

~~~
　　$('h1').html();          //取出h1的值
　　$('h1').html('Hello');   //对h1进行赋值
---
.html()      //取出或设置html内容
.text()      //取出或设置text内容
.attr()      //取出或设置某个属性的值
.width()     //取出或设置某个元素的宽度
.height()    //取出或设置某个元素的高度
.val()       //取出某个表单元素的值
~~~

