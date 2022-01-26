<template>
  <footer class="footer d-flex">
    <div class="inner-footer w-90 d-flex">
      <FooterLeft />
      <FooterRight />
    </div>
  </footer>
</template>

<script>
import FooterLeft from "./footer-component/FooterLeft.vue";
import FooterRight from "./footer-component/FooterRight.vue";
export default {
  name: "Footer",
  components: {
    FooterLeft,
    FooterRight,
  },
};
</script>

<style lang="scss">
.footer {
  position: relative;
  margin: 5em 0;
  justify-content: center;
}
</style>
