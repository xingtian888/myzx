<template>
    <div>
        <h2 @click="showname" >学校名称{{name }}</h2>
        <h2>地址{{address }}</h2>
    </div>
</template>

<script>
import {mixin} from "./mixin"

export default {
     name:'School',
     data(){
        return  {
           name:"尚硅谷",
           address:"北京昌平"
        }
     },
     methods:{
        showname1(){
            console.info(this.name)
        }
     },
     mixins:[mixin]



}
</script>

<style>

</style>