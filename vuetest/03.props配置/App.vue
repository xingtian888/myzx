<template>
   <div>
      <h2 ref="welcome">欢迎学习 {{msg}}</h2>
       
      <button ref="btn" @click="showDOM">点我输出上方的DOM元素</button>
      <Student ref="stu" name="张三" sex="男" :age=18 /><br/>
      <Student ref="stu2" name="李四" sex="女" :age=19 />
      
 
   </div>
</template>

<script>
    import Student from './components/Student.vue';
 

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
			console.log(this.$refs.stu) //School组件的实例对象（vc）
      }
    },
    components: {
       Student
    }
    

}
</script>

<style>

</style>