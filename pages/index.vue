<template>
	<div>
		<Header />
		<div>
			<Section />
			<Article />
		</div>
		<Footer />
	</div>
</template>

<script>

import Header from '~/components/Header.vue'
import Section from '~/components/Section.vue'
import Footer from '~/components/Footer.vue'
import Article from '~/components/Article.vue'
export default {
  components: { Header, Section, Footer, Article },}
</script>

<style scoped>
	
</style>