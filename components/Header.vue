<template>
	<header>
		<h1>Bypass LOGO</h1>
		<div>
			<a>HACKERTOOLS</a>
			<a>DOCUMENTATION</a>
		</div>
	</header>
</template>

<script>
export default {
	name:'Header'
}
</script>

<style scoped>
	header {

		/*TEST */
		border: 1px white solid;
		
		/* NAV */
		display: flex;
  		flex-direction: row;
		flex-wrap: nowrap;
  		justify-content: space-between;
  		align-items: stretch;
  		align-content: normal;
	}
</style>
