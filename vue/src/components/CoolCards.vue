<template>
  <div class="card">
    <h2 class="cardtitle">{{ title }}</h2>
    <img class="cardimg" v-bind:src="image" alt="" />
    <p class="cardprice">{{ Price }}</p>
    <p class="carddetails">{{ detail }}</p>
  </div>
</template>

<script>
export default {
  name: "CoolCard",
  props: {
    title: String,
    Price: String,
    image: String,
    detail: String,
  },
};
</script>

<style scoped>
*,
html,
body {
  box-sizing: border-box;
  margin: 0px;
  padding: 0px;
}
.card {
  display: flex;
  flex-direction: row;
  text-align: center;
  background-color: aqua;
  color: white;
}
.cardimg {
  height: 10%;
  width: 10%;
}
</style>
