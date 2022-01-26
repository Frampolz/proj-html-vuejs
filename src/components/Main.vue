<template>
  <main class="main d-flex">
    <OurProd :productArray="products" />
    <Service />
    <AllProd :productArray="products" />
    <Delivery />
    <Locations />
    <StayInTouch />
    <Shop />
  </main>
</template>

<script>
import OurProd from "./main-component/OurProd.vue";
import Service from "./main-component/Service.vue";
import AllProd from "./main-component/AllProd.vue";
import Delivery from "./main-component/Delivery.vue";
import Locations from "./main-component/Locations.vue";
import StayInTouch from "./main-component/StayInTouch.vue";
import Shop from "./main-component/Shop.vue";
export default {
  name: "Main",
  data() {
    return {
      products: [
        {
          item: "choco chip cookies",
          image: "choco-chip-cookies",
          category: "coockies, pastries",
          prize: "$19.00 $39.00",
        },
        {
          item: "strawberry jam cookies",
          image: "strawberry-jam-cookies",
          category: "coockies, pastries",
          prize: "$24.00- $62.00",
        },
        {
          item: "strawberry donut",
          image: "strawberry-donut",
          category: "donuts, pastries",
          prize: "$24.00- $42.00",
        },
        {
          item: "perfect macarons",
          image: "perfect-macarons",
          category: "macarons, pastries",
          prize: "$18.00- $52.00",
        },
        {
          item: "cookies with ice cream",
          image: "cookies-with-ice-cream",
          category: "cookies, pastries",
          prize: "$20.00- $48.00",
        },
        {
          item: "cherry cake",
          image: "cherry-cake",
          category: "cakes, pastries",
          prize: "$30.00- $62.00",
        },
        {
          item: "blackberry stuffed bread",
          image: "blackberry-stuffed-bread",
          category: "breads, cakes, pastries",
          prize: "$10.00- $32.00",
        },
        {
          item: "glazed pancake with lemon",
          image: "glazed-pancake-with-lemon",
          category: "pancake, cakes, pastries",
          prize: "$11.00- $33.00",
        },
        {
          item: "home bread",
          image: "home-bread",
          category: "breads, pastries",
          prize: "$13.00- $28.00",
        },
        {
          item: "premium bread",
          image: "premium-bread",
          category: "breads",
          prize: "$8.00- $20.00",
        },
        {
          item: "small cupcake",
          image: "small-cupcake",
          category: "cupcake, cakes, pastries",
          prize: "$12.50- $22.50",
        },
      ],
    };
  },
  components: {
    OurProd,
    Service,
    AllProd,
    Delivery,
    Locations,
    StayInTouch,
    Shop,
  },
};
</script>

<style lang="scss">
.main {
  margin-top: 10em;
  align-items: center;
  flex-direction: column;
}
</style>
