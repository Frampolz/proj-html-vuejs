<template>
  <div class="stay-in-touch w-90">
    <div class="stay-in-touch-container d-flex">
      <div class="stay-in-touch-box">
        <img src="../../assets/img/social-1.jpg" alt="" />
      </div>
      <div class="stay-in-touch-box d-flex">
        <h5>made for sharing</h5>
        <h2 class="m-05">let's stay in touch</h2>
        <div class="button m-05">
          <a class="btn purple" href=""
            ><i class="fab fa-instagram"></i>follow us</a
          >
        </div>
      </div>
      <div class="stay-in-touch-box">
        <img src="../../assets/img/social-2.jpg" alt="" />
      </div>
      <div class="stay-in-touch-box">
        <img src="../../assets/img/social-3.jpg" alt="" />
      </div>
      <div class="stay-in-touch-box">
        <img src="../../assets/img/social-4.jpg" alt="" />
      </div>
      <div class="stay-in-touch-box">
        <img src="../../assets/img/social-5.jpg" alt="" />
      </div>
      <div class="stay-in-touch-box">
        <img src="../../assets/img/social-6.jpg" alt="" />
      </div>
    </div>
  </div>
</template>

<script>
export default {
  name: "StayInTouch",
};
</script>

<style lang="scss">
@import "../../assets/scss/partials/variables.scss";
.stay-in-touch {
  margin-top: 10em;
  .stay-in-touch-container {
    gap: 2em;
    flex-wrap: wrap;
    .stay-in-touch-box {
      flex-basis: calc((100% / 3.93) - 2em);

      img {
        width: 100%;
      }
      &:nth-of-type(2) {
        flex-basis: calc(100% / 2.04);
        flex-direction: column;
        align-items: center;
        justify-content: center;
        background-color: $lightPurple;
        .fa-instagram {
          margin-right: 0.5em;
        }
      }
    }
  }
}
</style>
