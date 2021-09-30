<template>
  <footer :class="{ 'footer-absolute': isIndex }">
    <p>Bypass - par Charles, Enzo, Nathan, Simon et Théo</p>
  </footer>
</template>

<script>
export default {
  name: "Footer",
  props: {
    isIndex: Boolean
  }
};
</script>

<style scoped>
footer {
  margin-top: 50px;
  margin-bottom: 30px;
}

.footer-absolute {
  margin-top: 0;
  margin-bottom: 0;
  position: absolute;
  bottom: 0;
}

footer p {
  font-size: 14px;
}
</style>
