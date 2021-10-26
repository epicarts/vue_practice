<template>
  <div class="hello">

    <!-- 자삭 컴포넌트의 최상위(루트)가 하나일 경우 상속이 일어남. -->
    <my-btn style="color: red;">btn</my-btn>
    
    <my-btn-2>
      <template #text> 
        <span>Apple</span> 
      </template>
      <template v-slot:icon>
        <span>(a)</span>
      </template>
    </my-btn-2>

    <!-- 상속 -->
    <MyBtn color="blue"/>
    <MyBtn color="#000000"/>

    <!-- 불가 -->
    <!-- <MyBtn color="123"/> 글자가 적혀있는 문자 데이터 x--> 
    <!-- <MyBtn :color="123"/> 데이터 바인딩을 해서 숫자로 인식되게 해야함.-->

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
