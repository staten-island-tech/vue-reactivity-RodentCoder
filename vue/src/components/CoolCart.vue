<template>
  <div class="history">
    <ul class="order">
        <li class="items">{{ items }}</li>
    </ul>
  </div>
</template>

<script>
import { cart } from './CoolCards.vue';
export default {
  data(){
    return cart
  },
  name: "CoolCart",
  props:{
    items: String
  }
};
</script>

<style scoped>

.order{
    text-align: center;
}

</style>
