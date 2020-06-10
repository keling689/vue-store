<template>
  <div class="hello">
    <father></father>
	
  </div>
</template>


<script>
import father from './communite/father.vue'
export default {
  name: "HelloWorld",
  props: {
    msg: String
  },
  components:{
	  father
  }
};
</script>

<!-- Add "scoped" attribute to limit CSS to this component only -->
<style scoped lang="scss">
h3 {
  margin: 40px 0 0;
}
ul {
  list-style-type: none;
  padding: 0;
}
li {
  display: inline-block;
  margin: 0 10px;
}
a {
  color: #42b983;
}
</style>
