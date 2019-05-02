<template>
  <div class="text-center" id="app">
    <h1>Word Translation</h1>
    <a href="http://translate.yandex.com/">Powered by Yandex.Translate</a>
    <br>
		<hr>
    <!-- When form submitted function translateText() is run -->
		<TranslateForm v-on:formSubmit="translateText"></TranslateForm>
    <hr>
    <br>
		<TranslateOutput v-text="translatedText"></TranslateOutput>
  </div>
</template>

<script>
import TranslateForm from './components/TranslateForm'
import TranslateOutput from './components/TranslateOutput'

export default {
  name: 'app',
  components:{
	TranslateForm,
	TranslateOutput
	},
	data: function(){
		return {
			translatedText: ''
		}
	},
	methods: {
		translateText: function(text, language){
			this.$http.get('https://translate.yandex.net/api/v1.5/tr.json/translate?key=trnsl.1.1.20181104T102320Z.a3fb9954e7544c8c.9b440f44d18ba210605f46825cd17fb833eaf247&lang='+language+'&text='+text)
			.then((response) => {
				this.translatedText = response.body.text[0];
			});
		}
	}
}
</script>

<style>
body {
  background: rgb(240, 196, 235);
}
</style>
