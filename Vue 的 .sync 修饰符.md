### 定义方
- 在想要触发事件修改props时,使用 $emit('update:props属性名', props属性增删改)
```
<template>
  <div>
    {{ money }}
    <button @click="$emit('update:money', money - 100)">消费100元</button>
  </div>
</template>

<script>
export default {
  data() {
    return {};
  },
  props: ["money"],
};
</script>

<style scoped></style>

```

### 传递方
- 在传递数据给props属性时,想要允许同步数据,加个.sync
```
import Demo from "./Demo.vue";

new Vue({
  data:{
    total: 1000,
  },
  components: { Demo },
  template: `
   <div>
      <Demo :money.sync='total'/>
   </div>
  `,
}).$mount("#app");
```

### 总结
- 本质是使用的eventbus在对象(组件)之间, 进行数据通信
- 传递方在传递数据的同时, 使用event对象监听自定义事件, 准备修改
- 定义方在触发事件修改数据时, 触发emit的自定义事件, 通知传递方修改自己的数据
