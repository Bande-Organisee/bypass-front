<template>
  <div class="content">
    <div class="content-main" :class="{ 'content-moved': isClicked }">
      <img class="logo" src="@/assets/Bypass-logo/cover.png" />
      <section>
        <Box
          v-for="(box, i) in boxData"
          :key="i"
          :title="box.title"
          :content="box.content"
          :isClicked="i == 0 ? isClicked : false"
          @click.native="i == 0 ? (isClicked = !isClicked) : goToDocs()"
        />
      </section>
    </div>
    <div class="console" :class="{ 'console-moved': isClicked }">
      <p>> Console</p>
      <Form />
    </div>
    <Footer />
  </div>
</template>

<script>
export default {
  transition: "slide",
  data() {
    return {
      boxData: [
        {
          title: "Tester son ip",
          content:
            "Remplissez le formulaire pour savoir si votre site est vulnérable"
        },
        {
          title: "Documentation",
          content: "Pour mieux vous informer sur la cybersécurité"
        }
      ],
      isClicked: false
    };
  },
  methods: {
    goToDocs() {
      this.$router.push("/docs");
    }
  }
};
</script>

<style scoped>

body {
  overflow: hidden;
}
.content {
  min-height: 100vh;

  display: flex;
  flex-direction: row;
  justify-content: center;
  align-items: center;
  align-content: center;

  position: relative;
}

.content-main {
  display: flex;
  flex-direction: column;
  justify-content: space-between;
  align-items: center;
  align-content: center;
  transition: 0.5s;

  position: absolute;
  right: 50%;
  transform: translateX(50%);
}

.content-main .logo {
  width: 500px;
  margin-bottom: 40px;
  margin-top: -75px;
}

.content-main section {
  width: 100%;

  display: flex;
  flex-direction: row;
  justify-content: center;
  align-items: center;
  align-content: center;

  gap: 75px;
}

.content-moved {
  right: 5%;
  transform: translateX(0%);
}

.console {
  width: 35%;
  min-height: 300px;
  border: solid 1px #7de38d;
  padding: 10px 20px;
  transition: 0.3s;
  overflow: hidden;

  position: absolute;

  left: 0%;
  transform: translateX(-110%);

  transition: 0.5s;
  margin-top: 20px;
}

.console > p {
  font-family: "Bree Serif", serif;
  font-size: 24px;
}

.console-moved {
  left: 5%;
  transform: translateX(0%);
}
</style>
