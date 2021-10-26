<template>
  <div class="btn" :style="{ backgroundColor: color }">
		<slot>btn default</slot>
  </div>
</template>

<script>
export default {
	inheritAttrs: false,
	created() {
		console.log(this.$attrs)
	},
	// MyBtb 컴포넌트가 실행될때 마치 속성처럼 사용가능
	// 부모-자식간의 데이터 통신!
	props: {
		color: {
			type: String,
			default: 'gray'
		}
	}
}
</script>

<style scoped>
.btn {
	display: inline-block;
	margin: 4px;
	padding: 6px;
	border-radius: 4px;
	background-color: gray;
	color: white;
	cursor: pointer;
}
</style>