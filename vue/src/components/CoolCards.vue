<template>
  <div class="card">
    <h2 class="cardtitle">{{ title }}</h2>
    <img class="cardimg" v-bind:src="image" alt="" />
    <p class="cardprice">{{ Price }}</p>
    <button @click="buy">Click Me!</button>
    <p class="carddetails">{{ detail }}</p>
  </div>
</template>

<script>
export default {
  name: "CoolCard",
  methods: {
    buy: function () {
      this.cart.push(this.Price);
      console.log(this.cart);
    },
  },
  data() {
    return {
      cart: [],
    };
  },
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
