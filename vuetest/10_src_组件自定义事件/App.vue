<template>
	<div>
		<h1 class="app">你好啊</h1>
		<School/>
		<Student ref="student"  @click.native="receiveName()" />
	</div>
</template>

<script>
	import Student from './components/Student'
	import School from './components/School'

	export default {
		name:'App',
		components:{School,Student},
		methods:{
              receiveName(name){
              console.info("receive ",name)
			}
		},
		mounted(){
			// this.$refs.student.$on('atguigu',this.receiveName) //绑定自定义事件
		}

	}
</script>

<style scoped>
	.app{
		background-color: gray;
		padding: 5px;
	}
</style>