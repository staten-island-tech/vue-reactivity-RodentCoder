<template>
  <div class="Home">
    <h1 class="header">Funny Shooter Game Shop</h1>
    <button @click="displaycart">Hm</button>
    <div class="Gallery">
      <CoolCard
        v-for="ultrakill in ultrakill"
        :key="ultrakill.name"
        :title="ultrakill.name"
        :Price="ultrakill.Price"
        :image="ultrakill.img"
        :detail="ultrakill.detail"
      ></CoolCard>
    </div>
  </div>
</template>
<script>
import { cart } from "../components/CoolCards.vue";
import CoolCard from "../components/CoolCards.vue";
export default {
  components: { CoolCard },
  computed: {
    displaycart: function () {
      cart.cart.forEach();
    },
  },
  data() {
    return {
      ultrakill: [
        {
          name: "Piercer",
          Price: "$10",
          img: "../images/Piercer.webp",
          detail: "Idk go nuts",
        },
        {
          name: "Marksman",
          Price: "$100000000",
          img: "../images/Marksman.webp",
          detail: "placeholder text",
        },
        {
          name: "Core-Eject Shotun",
          Price: "$100000",
          img: "./images/Core_Shotgun.webp",
          detail: "placeholder text",
        },
        {
          name: "Pump Shotgun",
          Price: "$100",
          img: "../images/Pump_Shotgun.webp",
          detail: "placeholder text",
        },
        {
          name: "Attractor",
          Price: "$100",
          img: "../images/Attractor_Nailgun.webp",
          detail: "placeholder text",
        },
        {
          name: "Overheat",
          Price: "$100",
          img: "../images/Overheat_Nailgun.webp",
          detail: "placeholder text",
        },
        {
          name: "Electric Railgun",
          Price: "$100",
          img: "../images/ChargedERail.webp",
          detail: "placeholder text",
        },
        {
          name: "Malicicous Railgun",
          Price: "$100",
          img: "../images/ChargedMRail.webp",
          detail: "placeholder text",
        },
        {
          name: "Screw Driver",
          Price: "$100",
          img: "../images/ChargedSRail.webp",
          detail: "placeholder text",
        },
      ],
    };
  },
};
</script>

<style>
.header {
  text-align: center;
}
.Gallery {
  display: flex;
  justify-content: space-evenly;
  flex-direction: row;
  align-items: center;
  flex-wrap: wrap;
  color: white;
}
</style>
