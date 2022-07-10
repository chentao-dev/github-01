## 声明对象
```
let a = {}

let a = new Object()
```



## 删除属性
```
delete 对象['属性']
```



## 查看属性
```
Object.keys(对象)                   // 查所有属性
Object.values(对象)                 // 查所有值
Object.entries(对象)                // 查所有键值对
对象['属性']                        // 查属性值
```



## 增加/修改属性
```
对象['属性'] = 值                   // 增/改属性
Object.assign(对象,{...})          // 批量增/改属性
```



## 属性是否存在
```
属性 in 对象                      // 属性是否存在
对象.hasOwnProperty(属性)         // 属性是否存在  (不看原型)
```

