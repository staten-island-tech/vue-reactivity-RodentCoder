<template>
  <div class="card">
    <h2 class="cardtitle">{{ title }}</h2>
    <img class="cardimg" v-bind:src="image" alt="" />
    <p class="cardprice">{{ Price }}</p>
    <button class="buy" @click="buy">Buy</button>
    <p class="carddetails">{{ detail }}</p>
  </div>
</template>

<script>
import { reactive } from "vue";
export { cart };
const cart = reactive({
  cart: [],
});
export default {
  name: "CoolCard",
  methods: {
    buy: function () {
      cart.cart.push(`${this.title}:` + `${this.Price}`);
      console.log(cart.cart);
    },
  },
  data() {
    return {
      cart,
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
.buy {
  background: #ff4742;
  border: 1px solid #ff4742;
  border-radius: 6px;
  box-shadow: rgba(0, 0, 0, 0.1) 1px 2px 4px;
  box-sizing: border-box;
  color: #ffffff;
  font-size: 16px;
  padding: 12px 14px;
  text-align: center;
}
</style>
