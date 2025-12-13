<template>
    <div>
        
        <h2 @click="showname" >学生姓名:{{name }}</h2>
        <h2>性别:{{sex }}</h2>
        <h2>年龄:{{myage }}</h2>
        
    </div>
</template>

<script>
 import {mixin} from "./mixin"
export default {
     name:'Student',
      
     data(){
        return  {
           schoolname:"尚硅谷",
           name : "张三",
           sex : "男",
           age: 18,
           myage:this.age+1
        }
     },
     methods:{
      //   showname(){
      //       console.info(this.name)
      //   }
     },
  
     mixins:[mixin]
        
}
</script>

<style>

</style>