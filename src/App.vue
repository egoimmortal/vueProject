<template>
	<NavCom></NavCom>
	<router-view/>
	<FooterCom></FooterCom>
</template>

<script lang="ts" setup>
import NavCom from '@/components/NavCom.vue';
import { onMounted } from 'vue';
import FooterCom from './components/FooterCom.vue';

onMounted(() => {
	let root = document.querySelector(':root') as HTMLElement;
	root.style.setProperty('--nowHeight', window.innerHeight * 0.8 + 'px');
});
</script>

<style lang="scss">
:root {
	--window-scale: 0;
	--nowHeight: 0;
}
#app {
	font-family: Avenir, Helvetica, Arial, sans-serif;
	-webkit-font-smoothing: antialiased;
	-moz-osx-font-smoothing: grayscale;
	text-align: center;
	color: #2c3e50;

	& > .container{
		height: var(--nowHeight);
	}
}

.center-and-center{
	display: flex;
	justify-content: center;
	align-items: center;
}
</style>