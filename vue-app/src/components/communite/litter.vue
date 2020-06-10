<template>
  <div class='litter' @click="litterClick">
	  弟组件{{home.name}}
	  <slot></slot>
  </div>
</template>

<script>
export default {
  name: 'litter',
  inject:['home'],
  data(){
    return {
		
	}
  },
  components: {
	  
  },
  created(){
	  
  },
  mounted(){
	  this.$bus.$on('big',this.bigCall)
  },
  methods: {
	  litterClick(){
		  this.$emit('litterCall','弟弟')
		  this.$parent.$emit('lit','弟弟呼叫兄长')
		  
	  },
	  
	  bigCall(e){
		  console.log(e)
	  }
  }
}
</script>
<style lang='scss' scoped>
	.litter{
		color:dodgerblue;
	}
</style>
