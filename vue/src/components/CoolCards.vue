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
  width: 2100%;
  border: 8px solid rgba(218, 95, 95, 0.878);
  margin-bottom: 10px;
  background-color: coral;
  text-align: center;
}
.cardimg {
  height: 15vh;
  width: 20vh;
}
</style>
