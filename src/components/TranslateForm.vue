<!-- 表单组件 -->
<template>
  <div id="translateForm">
  	<div>
  		<form class="well" v-on:submit="formSubmit">
	  		<input class="form-control" type="text" v-model="textToTranslate" placeholder="请输入要翻译的内容！">
	  		<select class="form-control" v-model="language">
	  			<option value="en">English</option>
	  			<option value="ru">Russian</option>
	  			<option value="ko">Korean</option>
	  			<option value="ja">Japanese</option>
	  		</select>
	  		<input class="btn btn-primary" type="submit" value="翻译">
	  	</form>
  	</div>
  </div>
</template>

<script>

export default {
  name: 'translateForm',
  data:function(){
  		return{
  			textToTranslate:'',
  			language:''
  		}
  },
  methods:{
  	formSubmit:function(e){
  		e.preventDefault();
  		if(this.textToTranslate==''){
  			alert('请输入要翻译的内容!');
  		}
  		else{
  			this.$emit('shujuchuanshu',this.textToTranslate,this.language);
  		}
  		// alert(this.textToTranslate);
  		
  	}
  },
  created:function(){
  	this.language = "en";
  }
  
}
</script>

<style>
	.form-control{
		width: 60% !important;
		margin:10px auto;
		text-align:center;
	}

	.btn{
		width: 60%;
		margin: 0 auto;
	}
</style>
