<template>
  <div></div>
</template>

<script>
export default {};
</script>

<style scoped></style>

<!-- <template>
  <div class="Home">
    <CoolButton @click="check">Test</CoolButton>
    <h1 v-if="alive">{{ students }} is a person</h1>
    <h1 v-else="alive">{{ students }} is not a person</h1>
    <h2>things to steal from him</h2>
    <li v-for="parts in vulablebodyparts" :key="parts">{{ parts }}</li>
    <input type="text" placeholder="type something" v-model="message" />
    <p>{{ message }}</p>
    <CoolCard
      v-for="pokemon in pokemons"
      :key="pokemon.name"
      :title="pokemon.name"
      :Region="pokemon.Region"
      :image="pokemon.img"
    ></CoolCard>
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
      pokemons: [
        {
          name: "Pinsar",
          Region: "Kanto",
          Look: "Ugly",
          competitive: "OU",
          img: "../images/Alt_Marksman.webp",
        },
        {
          name: "Victreebel",
          Region: "Kanto",
          Look: "Actually Ugly",
          competitive: "PU",
          img: "https://assets.pokemon.com/assets/cms2/img/pokedex/full/071.png",
        },
        {
          name: "Galvantula",
          Region: "Unova",
          Look: "Cool",
          competitive: "RU",
          img: "https://assets.pokemon.com/assets/cms2/img/pokedex/full/596.png",
        },
        {
          name: "Celebi",
          Region: "Johto",
          Look: "Kinda Cute",
          competitive: "UU",
          img: "https://assets.pokemon.com/assets/cms2/img/pokedex/full/251.png",
        },
        {
          name: "Kyogre",
          Region: "Johto",
          Look: "Goofy",
          competitive: "Uber",
          img: "https://static.wikia.nocookie.net/pokemon/images/4/41/382Kyogre.png/revision/latest?cb=20201003100403",
        },
        {
          name: "Volcarona",
          Region: "Unova",
          Look: "Cute",
          competitive: "OU",
          img: "https://static.pokemonpets.com/images/monsters-images-800-800/2637-Shiny-Volcarona.webp",
        },
        {
          name: "Chandelure",
          Region: "Unova",
          Look: "Awesome",
          competitive: "UU",
          img: "https://archives.bulbagarden.net/media/upload/thumb/9/97/0609Chandelure.png/250px-0609Chandelure.png",
        },
      ],
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
</script> -->
