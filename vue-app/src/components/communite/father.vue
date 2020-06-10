<template>
  <div class='father'>
	  父组件
	  <big @bigCall="bigBack">兄</big>
	  <litter @litterCall="litterBack">弟</litter>
  </div>
</template>

<script>
import big from './big.vue'
import litter from './litter.vue'
export default {
  name: '',
  data(){
    return {
		
	}
  },
  components: {
	  big,
	  litter
  },
  created(){
	  
  },
  mounted(){
	  
  },
  methods: {
	  bigBack(e){
			console.log(e)
	  },
	  litterBack(e){
		  console.log(e)
	  }
  }
}
</script>
<style lang='scss' scoped>
</style>
