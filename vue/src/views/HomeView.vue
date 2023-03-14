<template>
  <div class="Home">
    <CoolButton @click="check">Test</CoolButton>

    <h1 v-if="alive">{{ students }} is a person</h1>
    <h1 v-else="alive">{{ students }} is not a person</h1>
    <h2>things to steal from him</h2>
    <ui>
      <li v-for="parts in vulablebodyparts" :key="parts">{{ parts }}</li>
    </ui>
    <input type="text" placeholder="type something" v-model="message" />
    <p>{{ message }}</p>
  </div>
</template>

<script>
import CoolButton from "../components/CoolButton.vue";
export default {
  name: "Home",
  components: { CoolButton },
  data() {
    return {
      message: "",
      students: "Daniel",
      vulablebodyparts: ["brain", "liver", "lungs", "kidney"],
      alive: true,
    };
  },
  methods: {
    check: function () {
      if (this.alive === true) {
        this.alive = false;
      } else {
        this.alive = true;
      }
    },
  },
};
</script>
