<template>
  <div class="hello">
    <my-btn>btn</my-btn>
    
    <my-btn-2>
      <template #text> 
        <span>Apple</span> 
      </template>
      <template v-slot:icon>
        <span>(a)</span>
      </template>
    </my-btn-2>
  </div>
</template>

<script>
import MyBtn from './MyBtn.vue'
import MyBtn2 from './MyBtn2.vue'

export default {
  name: 'HelloWorld',
  components: {
    MyBtn,
    MyBtn2
  },
  props: {
    msg: String
  }
}
</script>

<!-- Add "scoped" attribute to limit CSS to this component only -->
<style scoped>
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
