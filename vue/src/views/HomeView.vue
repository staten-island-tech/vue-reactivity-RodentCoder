<template>
  <div class="Home">
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
          detail: "placeholder text",
        },
        {
          name: "Marksman",
          Price: "$100",
          img: "../images/Marksman.webp",
          detail: "placeholder text",
        },
        {
          name: "Core-Eject Shotun",
          Price: "$100",
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
.Gallery {
  display: flex;
  justify-content: space-evenly;
  flex-direction: row;
  align-items: center;
  flex-wrap: wrap;
  color: white;
}
</style>
