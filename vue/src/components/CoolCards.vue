<template>
  <div class="card">
    <h2>{{ title }}</h2>
    <img v-bind:src="image" alt="" />
    <p>{{ Price }}</p>
  </div>
</template>

<script>
export default {
  name: "CoolCard",
  props: {
    title: String,
    Price: String,
    image: String,
  },
};
</script>

<style scoped>
.card {
  display: flex;
  flex-direction: row;
  background-color: aqua;
  color: white;
}
</style>
