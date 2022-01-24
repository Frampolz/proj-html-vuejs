<template>
  <main class="main d-flex">
    <OurProd />
    <Service />
  </main>
</template>

<script>
import OurProd from "./main-component/OurProd.vue";
import Service from "./main-component/Service.vue";
export default {
  name: "Main",
  components: {
    OurProd,
    Service,
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
