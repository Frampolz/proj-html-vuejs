<template>
  <main class="main d-flex">
    <OurProd />
  </main>
</template>

<script>
import OurProd from './main-component/OurProd.vue'
export default {
  name: "Main",
  components: {
    OurProd
  }
};
</script>

<style lang="scss">
.main {
  margin-top: 10em;
  justify-content: center;
}
</style>
