<template>
     <div>
         <h2>姓名:{{name}}</h2>
         <h2>年龄:{{age}}</h2>
     </div>
</template>
  
<script lang="javascript" >
      
    export  default  {
         name : "student",
         data(){
             return {
                      name : "张三",
                      age :18

              }
          }
     }
 
//    export { school };
//    export default school //默认暴露
</script>


<style>

</style>