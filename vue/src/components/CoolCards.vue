<template>
  <div class="card">
    <h2>{{ title }}</h2>
    <img v-bind:src="image" alt="" />
    <p>{{ description }}</p>
  </div>
</template>

<script>
export default {
  name: "CoolCard",
  props: {
    title: String,
    description: String,
    image: String,
  },
};
</script>

<style scoped>
.card {
  background-color: aqua;
  color: white;
}
</style>
