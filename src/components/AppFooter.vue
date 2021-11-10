<template>
	<div class="layout-footer">
		<img alt="Logo" src="images/logo-white.svg" height="40" class="mr-2" />
		by
		<span class="font-medium ml-2">PrimeVue</span>
	</div>
</template>

<script>
	export default {
		name: "AppFooter",
		computed: {
			darkTheme() {
				//return this.$appState.theme.startsWith('saga');
                return false
			}
		}
	}
</script>

<style scoped>
</style>