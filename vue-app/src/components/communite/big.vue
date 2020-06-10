<template>
  <div class='big' @click="bigClick">
	  兄组件
	  <slot></slot>
  </div>
</template>

<script>
export default {
  name: 'big',
  data(){
    return {
		
	}
  },
  components: {
	  
  },
  created(){
	  
  },
  mounted(){
	  this.$parent.$on('lit',this.litBack)
	  
  },
  methods: {
	  bigClick(){
		  this.$emit('bigCall','兄长')
		  this.$bus.$emit('big','兄长呼叫弟弟')
	  },
	  litBack(e){
		  console.log(e)
	  }
	  
  }
}
</script>
<style lang='scss' scoped>
.big{
	color:red;
}
</style>
