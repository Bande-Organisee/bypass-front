<template>
  <div>
    <form @submit.prevent="getData(ipInput, portInput)">
      <input type="text" v-model="ipInput" placeholder="ip" />
      <input type="number" v-model="portInput" placeholder="port" />
      <input type="submit" value="tester" />
    </form>

    <div>
      <p>
        $nmap -Pn -p {{ portInput }} {{ ipInput }}
        <span v-if="response"
          ><br />
          <br />{{ response }}</span
        ><span class="blink">_</span>
      </p>
    </div>
  </div>
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
        .get(`https://workshop.sbcorp.ovh:3842/getIp?ip=${ip}&port=${+port}`)
        .then(response => (this.response = response.data));
    }
  }
};
</script>

<style scoped>
form {
  display: flex;
  flex-direction: row;
  justify-content: flex-start;
  align-items: center;
  align-content: center;

  gap: 25px;
}

form input {
  font-family: "Open Sans", sans-serif;
  background: none;
  outline: none;
  border: none;
  font-size: 16px;
  color: #7de38d;
  border-bottom: solid 1px #7de38d;
  padding: 6px 0px;
}

/* Chrome, Safari, Edge, Opera */
input::-webkit-outer-spin-button,
input::-webkit-inner-spin-button {
  -webkit-appearance: none;
  margin: 0;
}

/* Firefox */
input[type="number"] {
  -moz-appearance: textfield;
}

form input[type="submit"] {
  border: solid 1px #7de38d;
  padding: 5px 10px;
  transition: 0.3s;
}

form input[type="submit"]:hover {
  cursor: pointer;
  background: #7de38d;
  color: #00242b;
}

form input::placeholder {
  color: #7de38d;
}

.blink {
  animation: 1.5s infinite blink;
}

@keyframes blink {
  0% {
    opacity: 1;
  }
  50% {
    opacity: 0;
  }
  100% {
    opacity: 1;
  }
}
</style>
