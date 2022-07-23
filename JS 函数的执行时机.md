## 解释为什么如下代码会打印 6 个 6

```javascript
let i = 0
for(i = 0; i<6; i++){
  setTimeout(()=>{
    console.log(i)
  },0)
}
```

因为每一轮循环, 都会在定时器这里停住, 等待任务队列执行完, 有空闲后再依次执行定时器, 由于最后才执行, 此时的变量 i 已经变成了6 , 所以会打印出666666



## 写出让上面代码打印 0、1、2、3、4、5 的方法

```javascript
// let结合for, 会自动在每个循环创建临时变量保存当前i
for(let i = 0; i<6; i++){
  setTimeout(()=>{
    console.log(i)
  },0)
}
```



