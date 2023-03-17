<template>
  <div class="Home">
    <CoolCard
      v-for="ultrakill in ultrakill"
      :key="ultrakill.name"
      :title="ultrakill.name"
      :Price="ultrakill.Price"
      :image="ultrakill.img"
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
      ultrakill: [
        {
          name: "Piercer",
          Price: "$100",
          img: "../images/Piercer.webp",
        },
        {
          name: "Marksman",
          Price: "$100",
          img: "../images/Marksman.webp",
        },
        {
          name: "Galvantula",
          Price: "$100",
          img: "",
        },
        {
          name: "Celebi",
          Price: "$100",
          img: "https://assets.pokemon.com/assets/cms2/img/pokedex/full/251.png",
        },
        {
          name: "Kyogre",
          Price: "$100",
          img: "https://static.wikia.nocookie.net/pokemon/images/4/41/382Kyogre.png/revision/latest?cb=20201003100403",
        },
        {
          name: "Volcarona",
          Price: "$100",
          img: "https://static.pokemonpets.com/images/monsters-images-800-800/2637-Shiny-Volcarona.webp",
        },
        {
          name: "Chandelure",
          Price: "$100",
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
</script>
