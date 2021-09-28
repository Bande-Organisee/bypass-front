<template>
	<div>
		<Header />
		<Section />
		<Footer />
	</div>
</template>

<script>

import Header from '~/components/Header.vue'
import Section from '~/components/Section.vue'
import Footer from '~/components/Footer.vue'
export default {
  components: { Header, Section, Footer },}
</script>

<style scoped>
	div {
	min-height: 100vh;
	display: flex;
	flex-direction: column;
	flex-wrap: nowrap;
	justify-content: space-between;
	align-items: center;
	align-content: center;
} 
</style>