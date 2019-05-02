<template>
  <div class="row justify-content-center" id="translateForm">
		<div class="col-md-6	 col-md-offset-3">
			<form id="transForm" class="form-inline well justify-content-center" v-on:submit="formSubmit">
				<input class="form-control" type="text" v-model="textToTranslate" placeholder="Enter a word...">
				<select class="form-control" v-model="language">
					<option value="ru">Russian</option>
					<option value="es">Spanish</option>
					<option value="fr">French</option>
					<option value="zh">Chinese</option>
          <option value="nl">Dutch</option>
          <option value="pt">Portuguese</option>
          <option value="la">Latin</option>
				</select>
				<input class="btn btn-info" type="submit" value="Translate">
			</form>
  	</div>
	</div>
</template>

<script>
export default {
  name: 'translateForm',
  data() {
	  return {
			textToTranslate:'',
			language: ''
		}
	},
	created() {
		this.language = "es"; /* default language shown */
	},
	methods: {
		formSubmit(e){
			this.$emit('formSubmit', this.textToTranslate, this.language);
			e.preventDefault();
		}
	}
}
</script>

<style>

  /* style applied to form using id */
	#transForm {
		border-radius: 10px;
		border: 2px rgb(110, 107, 107) solid;
	}
</style>
