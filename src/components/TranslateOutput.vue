<!-- 展示翻译结果 -->
<template>
	<div class="result" id="translateOutput">
		<h1>{{translatedText}}</h1>
	</div>
</template>
<script>
	export default{
		name:'translateOutput',
		props:[
			"translatedText"
		]

	}
</script>
<style scoped>
	.result{
		display: inline-block;
		margin-top: 50px;
		color: #f7021d;
		font-size: 30px !important;
		border-bottom: 1px solid #000;
	}
</style>