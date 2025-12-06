#                    硅谷甄选运营平台

此次教学课程为硅谷甄选运营平台项目,包含运营平台项目模板从0到1开发，以及数据大屏幕、权限等业务。

此次教学课程涉及到技术栈包含***:vue3+TypeScript+vue-router+pinia+element-plus+axios+echarts***等技术栈。

## 一、vue3组件通信方式

**通信仓库地址:https://gitee.com/jch1011/vue3_communication.git**

不管是vue2还是vue3,组件通信方式很重要,不管是项目还是面试都是经常用到的知识点。

**比如:vue2组件通信方式**

**props:**可以实现父子组件、子父组件、甚至兄弟组件通信

**自定义事件**:可以实现子父组件通信

**全局事件总线$bus**:可以实现任意组件通信

**pubsub:**发布订阅模式实现任意组件通信

**vuex**:集中式状态管理容器，实现任意组件通信

**ref**:父组件获取子组件实例VC,获取子组件的响应式数据以及方法

**slot:**插槽(默认插槽、具名插槽、作用域插槽)实现父子组件通信........

### 1.1props

props可以实现父子组件通信,在vue3中我们可以通过defineProps获取父组件传递的数据。且在组件内部不需要引入defineProps方法可以直接使用！

**父组件给子组件传递数据**

```
<Child info="我爱祖国" :money="money"></Child>
```

**子组件获取父组件传递数据:方式1**

```
let props = defineProps({
  info:{
   type:String,//接受的数据类型
   default:'默认参数',//接受默认数据
  },
  money:{
   type:Number,
   default:0
}})
```

**子组件获取父组件传递数据:方式2**

```
let props = defineProps(["info",'money']);
```

子组件获取到props数据就可以在模板中使用了,但是切记props是只读的(只能读取，不能修改)