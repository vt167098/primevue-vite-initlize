<template>
	<div class="layout-topbar">
		<router-link to="/" class="layout-topbar-logo">
			<img alt="Logo" src="images/gfclogo.jpg" />
			<span>Program Title</span>
		</router-link>
		<button class="p-link layout-menu-button layout-topbar-button" @click="onMenuToggle">
			<i class="pi pi-bars"></i>
		</button>

		<ul class="layout-topbar-menu hidden lg:flex origin-top">
			<li>
				<button class="p-link layout-topbar-button">
					<i class="pi pi-calendar"></i>
					<span>通知</span>
				</button>
			</li>
			<li>
				<button class="p-link layout-topbar-button">
					<i class="pi pi-cog"></i>
					<span>設定</span>
				</button>
			</li>
			<li>
				<button class="p-link layout-topbar-button">
					<i class="pi pi-user"></i>
					<span>帳戶</span>
				</button>
			</li>
		</ul>
	</div>
</template>

<script>
import 'primevue/resources/themes/saga-blue/theme.css'
import 'primevue/resources/primevue.css'
import 'primeicons/primeicons.css'
import 'primeflex/primeflex.css'

export default {
    methods: {
        onMenuToggle(event) {
            this.$emit('menu-toggle', event);
        },
		onTopbarMenuToggle(event) {
            this.$emit('topbar-menu-toggle', event);
        }
    },
	computed: {
		darkTheme() {
		//	return this.$appState.theme.startsWith('saga-blue');
			return false
		}
	}
}
</script>