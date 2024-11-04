<template>
	<h1 class="text-white text-2xl mb-2">Formkit Example</h1>
	<p class="text-white mb-8">Icon works fine in Password, checkbox fails to render check mark.</p>

	<FormKit type="form">
		<FormKit
			type="password"
			label="A fancy password input"
			value="mySecretPassword!"
			prefix-icon="password"
			suffix-icon="eyeClosed"
			@suffix-icon-click="handleIconClick"
			suffix-icon-class="hover:text-blue-500"
		/>
		<FormKit
			type="checkbox"
			label="Terms and Conditions"
			help="Do you agree to our terms of service?"
			name="terms"
			:value="true"
			validation="accepted"
			validation-visibility="dirty"
		/>
	</FormKit>
</template>

<script lang="ts" setup>
const handleIconClick = (node, e) => {
	node.props.suffixIcon = node.props.suffixIcon === 'eye' ? 'eyeClosed' : 'eye'
	node.props.type = node.props.type === 'password' ? 'text' : 'password'
}
</script>

<style>
body { background: #222; margin: 16px }
</style>
