<template>
  <div class="btn">
		<slot name="icon">(s)</slot>
		<slot name="text">defalut btn2</slot>
  </div>
</template>

<script>
export default {

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