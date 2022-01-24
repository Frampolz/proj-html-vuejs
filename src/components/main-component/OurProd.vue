<template>
  <div class="our-prod w-90 d-flex">
    <div class="our-prod-box">
      <div class="inner-our-prod-box">
        <h5>our products</h5>
        <h2>
          All our delectable pastries are backed fresh in our Kitchen very
          morning, and are made with all- natural, all organic ingredients.
        </h2>
        <div class="button"><a href="">start shopping</a></div>
      </div>
    </div>
    <div class="our-prod-box">
      <img src="../../assets/img/choco-chip-cookies.jpg" alt="" />
    </div>
    <div class="our-prod-box">
      <img src="../../assets/img/strawberry-jam-cookies.jpg" alt="" />
    </div>
  </div>
</template>

<script>
export default {
  name: "OurProd",
};
</script>

<style lang="scss">
@import "../../assets/scss/partials/variables.scss";
.our-prod {
  gap: 1em;
  .our-prod-box {
    flex-basis: calc(100% / 3);

    img {
      width: 100%;
    }
  }
  .inner-our-prod-box {
      h2 {
          padding-right: 3em;
      }
    .button {
      display: inline-block;
      margin-top: 2em;
      a {
        padding: 0.7em 1.7em;
        border-radius: 5px;
        background-color: $purple;
        font-size: 1.1em;
        color: white;
      }
    }
  }
}
</style>
