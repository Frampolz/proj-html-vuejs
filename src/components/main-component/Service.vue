<template>
  <div class="service w-90 d-flex">
    <div class="heading">
      <h5>corporate &amp; weddings</h5>
      <h2>baking special moment</h2>
    </div>
    <div class="service-box-container d-flex">
      <div class="service-box">
        <img src="../../assets/img/corporate-bg.jpg" alt="" />
      </div>
      <div class="service-box">
        <img src="../../assets/img/wedding-bg.jpg" alt="" />
      </div>
    </div>
  </div>
</template>

<script>
export default {
  name: "Service",
};
</script>

<style lang="scss">
.service {
  margin-top: 12em;
  flex-direction: column;
  .heading {
    text-align: center;
    h2 {
      text-transform: capitalize;
    }
  }
  .service-box-container {
    gap: 8em;
    .service-box {
      flex-basis: calc(100% / 2);
      img {
        width: 100%;
        border-radius: 4px;
      }
    }
  }
}
</style>
