<template>
  <header>
    <img
      class="logo"
      src="@/assets/Bypass-logo/cover-ajusted.png"
      @click="$router.push('/')"
    />
    <div>
      <NuxtLink class="link" to="/">Accueil</NuxtLink>
    </div>
  </header>
</template>

<script>
export default {
  name: "Header"
};
</script>

<style scoped>
header {
  display: flex;
  flex-direction: row;
  justify-content: space-between;
  align-items: center;
  align-content: center;
  margin-top: 25px;
}

.logo {
  width: 150px;
}

.logo:hover {
  cursor: pointer;
}

.link {
  color: #7de38d;
  font-size: 28px;
}

</style>
