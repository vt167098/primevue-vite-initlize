<template>
	<div class="layout-menu-container">
		<AppSubmenu :items="model" class="layout-menu" :root="true" @menuitem-click="onMenuItemClick" />
		<a href="https://www.primefaces.org/primeblocks-vue" class="block mt-3">
			<img alt="primeblocks" src="images/banner-primeblocks-dark.png" class="w-full" />
		</a>
	</div>
</template>

<script>
import AppSubmenu from '../components/AppSubmenu.vue'

export default {
	props: {
		model: Array
	},
    methods: {
        onMenuItemClick(event) {
            this.$emit('menuitem-click', event);
        }
    },
	computed: {
		darkTheme() {
			//return this.$appState.theme.startsWith('saga');
            return false
		}
	},
	components: {
		'AppSubmenu': AppSubmenu
	}
}
</script>

<style scoped>
</style>