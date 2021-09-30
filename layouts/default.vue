<template>
  <div class="wrapper">
    <Nuxt />
  </div>
</template>

<style scoped>
.page-enter-active,
.page-leave-active {
  transition: opacity 0.3s;
}
.page-enter,
.page-leave-to {
  opacity: 0;
}

.layout-enter-active,
.layout-leave-active {
  transition: opacity 0.2s;
}
.layout-enter,
.layout-leave-to {
  opacity: 0;
}

.slide-enter-active,
.slide-leave-active {
  transition: opacity 0.4s ease-in-out, transform 0.4s ease-in-out;
}
.slide-enter,
.slide-leave-to {
  opacity: 0;
  transform: translate3d(-100px, 0, 0);
}
</style>
