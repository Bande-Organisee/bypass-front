<template>
  <div class="content">
    <Header />
    <hr />
    <h1>Documentation</h1>

    <p>
      C'est ici que vous trouverez des liens utiles vous permettant de vous
      renseigner sur le vaste sujet de la cybersécurité
    </p>
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
    test() {
      alert("zreiuphfezh");
    }
  }
};
</script>

<style scoped>
.content {
  min-height: 100vh;
  padding: 0px 20%;
  transition: 0.3;
}

.content hr {
  border: 0;
  border-top: 1px solid #7de38d;
  margin-bottom: 40px;
  margin-top: 25px;
}
</style>
