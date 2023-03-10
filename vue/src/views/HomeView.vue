<template>
  <div class="Home">
    <h1 v-if="alive">{{ students }} is a person</h1>
    <h1 v-else="alive">{{ students }} is not a person</h1>
    <h2>things to steal from him</h2>
    <ui>
      <li v-for="parts in vulablebodyparts" :key="parts">{{ parts }}</li>
    </ui>
  </div>
</template>

<script>
export default {
  name: "Home",
  components: {},
  data() {
    return {
      students: "Daniel",
      vulablebodyparts: ["brain", "liver", "lungs", "kidney"],
      alive: true,
    };
  },
  methods: {
    alive: function () {
      if (this.alive === true) {
        this.alive = false;
      } else {
        this.alive = true;
      }
    },
  },
};
</script>
