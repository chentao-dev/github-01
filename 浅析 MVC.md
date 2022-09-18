# MVC 三个对象分别做什么
- M 数据层
- V 视图层
- C 控制层
- 主要是为了大型项目时, 恒定复杂度, 以后增加再多功能, 代码也不会很冗余, 重复率少
```
let m = {
    data: {},
    create(){},
    delete(){},
    update(){},
    get(){}
}

let v = {
    el: null,
    template: ``,
    init(对象){ v.el = 对象 },
    render(data数据){ 更新页面 }
}

let c ={
    init(对象){
        v.init(对象)
        v.render(data数据)
        c.bindEvents()
    },
    bindEvents(){对象绑定事件}
}

export default c
```


# view=render(data) 概念
- 原本用户每次触发事件, 改变页面数据, 都会用dom操作去读/写页面元素渲染页面
- 使用render(data)后, 每次触发事件, 都会修改内存中的data, 再把data渲染至页面, 不需要dom操作


# EventBus 有哪些 API，是做什么用的
- eventbus.on(自定义事件,函数) &emsp;   // 监听事件
- eventbus.off(自定义事件,函数) &emsp;  // 移除事件
- eventbus.trigger(自定义事件) &emsp;   // 触发事件
- 用于在不同对象之间通信
- 比如想要在M层调用V层的方法, 又不能写在M层里, 就可以写在C层里给eventbus监听事件去调用V层的方法, 让M层去触发eventbus的事件


# 表驱动编程是做什么的
- 是为了简化代码
- 把不同的参数抽成对象, 把重复的逻辑代码抽成函数, 遍历对象拿到参数和函数名
- 当存在大批重复, 但又不完全重复的代码时, 就可以使用表驱动编程


# 如何理解模块化
- 最小知识原则, 可以避免了解其他不相关的代码, 有利于代码回顾, 以及团队分工合作,
- 写完自己的模块提供接口, 别人只需要引入模块调用接口就能使用了

# 事不过三原则
- 代码重复三次抽成函数
- 属性重复三次抽成类
- 创建对象重复三次使用继承