<template>
  <div class="Home">
    <CoolButton @click="check">Test</CoolButton>
    <h1 v-if="alive">{{ students }} is a person</h1>
    <h1 v-else="alive">{{ students }} is not a person</h1>
    <h2>things to steal from him</h2>
    <li v-for="parts in vulablebodyparts" :key="parts">{{ parts }}</li>
    <input type="text" placeholder="type something" v-model="message" />
    <p>{{ message }}</p>
    <CoolCard
      title="hello words"
      description="man"
      image="https://previews.123rf.com/images/nickp37/nickp371202/nickp37120200104/12295296-two-men.jpg"
    />
  </div>
</template>

<script>
import CoolButton from "../components/CoolButton.vue";
import CoolCard from "../components/CoolCards.vue";
export default {
  name: "Home",
  components: { CoolButton, CoolCard },
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
