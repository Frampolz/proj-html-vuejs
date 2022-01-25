<template>
  <main class="main d-flex">
    <OurProd />
    <Service />
    <AllProd />
    <Delivery />
  </main>
</template>

<script>
import OurProd from "./main-component/OurProd.vue";
import Service from "./main-component/Service.vue";
import AllProd from "./main-component/AllProd.vue";
import Delivery from "./main-component/Delivery.vue";
export default {
  name: "Main",
  components: {
    OurProd,
    Service,
    AllProd,
    Delivery
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
