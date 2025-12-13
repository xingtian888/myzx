<template>
    <div>
        <h2>欢迎到{{schoolname}}</h2>
        <h2>学生姓名:{{name }}</h2>
        <h2>性别:{{sex }}</h2>
        <h2>年龄:{{myage }}</h2>
        <button @click="changeAge">修改年龄</button>
    </div>
</template>

<script>
export default {
     name:'Student',
     data(){
        return  {
           schoolname:"尚硅谷",
           myage:this.age+1
        }
     },
     methods:{
        changeAge(){
            this.myage=this.myage+1
        }
     },
    //  props:["name","sex","age"]  //简单接受

     //指定类型
     props:{
        name : String,
        sex:String,
        age:Number
     }

}
</script>

<style>

</style>