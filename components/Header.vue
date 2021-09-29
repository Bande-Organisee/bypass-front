<template>
	<header>
		<img id="logo" src="../assets/Bypass-logo/cover.png">
		<div id="text">
			<a href="#">HACKERTOOLS</a>
			<a href="#">DOCUMENTATION</a>
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
		
		/* FLEXBOX*/

		display: flex;
  		flex-direction: row;
		flex-wrap: nowrap;
  		justify-content: space-between;
  		align-items: center;
  		align-content: normal;
	}

	a{
		margin: 30px;
	}

	#logo{
		height: 50px;
	}

</style>
