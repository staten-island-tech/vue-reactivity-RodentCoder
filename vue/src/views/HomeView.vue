<template>
  <div class="Home">
    <h1 class="header">Funny Shooter Game Shop</h1>
    <div class="order">
      <h2 class="history" v-for="carts in cart" :key="cart">{{ carts }}</h2>
    </div>
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
import CoolCart from "../components/CoolCart.vue";

function yes() {
  let shop = Object.values(cart);
  return shop;
}
yes();

export default {
  components: { CoolCard, CoolCart },
  data() {
    return {
      cart,
      ultrakill: [
        {
          name: "Piercer",
          Price: "$10",
          img: "/Piercer.webp",
          detail: "Gun go shoot",
        },
        {
          name: "Marksman",
          Price: "$100",
          img: "/Marksman.webp",
          detail: "The Spare Change in my back packet",
        },
        {
          name: "Core-Eject Shotun",
          Price: "$150",
          img: "/Core_Shotgun.webp",
          detail: "Gun go Boom",
        },
        {
          name: "Pump Shotgun",
          Price: "$150",
          img: "/Pump_Shotgun.webp",
          detail: "Self Boom",
        },
        {
          name: "Attractor",
          Price: "$300",
          img: "/Attractor_Nailgun.webp",
          detail: "Nails",
        },
        {
          name: "Overheat",
          Price: "$300",
          img: "/Overheat_Nailgun.webp",
          detail: "Nail go Brrrr",
        },
        {
          name: "Electric Railgun",
          Price: "$500",
          img: "/ChargedERail.webp",
          detail: "Laser",
        },
        {
          name: "Malicicous Railgun",
          Price: "$500",
          img: "/ChargedMRail.webp",
          detail: "Exolsoping Laser",
        },
        {
          name: "Screw Driver",
          Price: "$500",
          img: "/ChargedSRail.webp",
          detail: "Useless",
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

.order {
  display: flex;
  justify-content: space-evenly;
  flex-direction: row;
  align-items: center;
  flex-wrap: wrap;
  height: 100% auto;
}
.history {
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
