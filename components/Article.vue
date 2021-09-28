<template>
  <article>
    <input type="text" v-model="ipInput" placeholder="ip" />
    <input type="text" v-model="portInput" placeholder="port" />
    <button @click="getData(ipInput, portInput)">test</button>
    <div v-if="response">
      <p>Réponse : {{ response }}</p>
    </div>
  </article>
</template>

<script>
import axios from "axios";

export default {
  name: "Article",
  data() {
    return {
      response: null,
      ipInput: "",
      portInput: ""
    };
  },
  methods: {
    getData(ip, port) {
      // 37.59.50.228
      // 8006
      console.log("scan");
      axios
        .get(`http://localhost:3842/getIp?ip=${ip}&port=${+port}`)
        .then(response => (this.response = response));
    }
  }
};
</script>

<style scoped>
article {
  /* TEST */
  border: 1px white solid;
  border-radius: 20px;
  background-color: #004d4e;
}
</style>
