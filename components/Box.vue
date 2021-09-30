<template>
  <div class="box" :class="{ 'box-clicked': isClicked }">
    <h1>> {{ title }}</h1>
    <p>
      {{ content }}
    </p>
  </div>
</template>

<script>
export default {
  name: "Box",
  props: {
    title: String,
    content: String,
    isClicked: Boolean
  }
};
</script>

<style scoped>
.box {
  width: 300px;
  height: 150px;
  border: solid 1px #7de38d;
  padding: 10px 20px;
  transition: 0.3s;
  overflow: hidden;
}

.box:hover {
  cursor: pointer;
  background: #7de38d;
  color: #00242b;
}

.box h1 {
  font-weight: normal;
  margin-bottom: 0;
}

.box h1:nth-child(2) {
  margin: 0;
}

.box-clicked {
  background: #7de38d;
  color: #00242b;
}
</style>
