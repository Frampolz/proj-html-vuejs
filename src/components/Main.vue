<template>
  <main class="main d-flex">
    <OurProd />
    <Service />
    <AllProd />
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
