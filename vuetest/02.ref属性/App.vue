<template>
   <div>
      <h2 ref="welcome">欢迎学习 {{msg}}</h2>
       
      <button ref="btn" @click="showDOM">点我输出上方的DOM元素</button>
      <School ref="sch"/>
   </div>
</template>

<script>
    import School from './components/School.vue'

export default {
    name: 'App',
    data(){
        return {
           msg: "VUE" 
        }
    },
    methods:{
      showDOM(){
         console.info(this.$refs.welcome)
         console.log(this.$refs.btn) //真实DOM元素
			console.log(this.$refs.btn.innerHTML) //真实DOM元素,获取button的文本内容
			console.log(this.$refs.sch) //School组件的实例对象（vc）
      }
    },
    components: {
       School
    }
    

}
</script>

<style>

</style>