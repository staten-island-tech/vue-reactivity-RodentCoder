<template>
  <div class="card">
    <h2 class="cardtitle">{{ title }}</h2>
    <img class="cardimg" v-bind:src="image" alt="" />
    <p class="cardprice">{{ Price }}</p>
    <p class="carddetails">{{ detail }}</p>
    <CoolButton></CoolButton>
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

.cardprice,
.carddetails {
  font-size: x-large;
}
.card {
  height: 40vh;
  width: 32vh;
  border: 8px solid rgba(218, 95, 95, 0.878);
  margin-bottom: 10px;
  margin: 20px;
  background-color: coral;
  text-align: center;
}
.cardimg {
  height: 15vh;
  width: 20vh;
}
</style>
