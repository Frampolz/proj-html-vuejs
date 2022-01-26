<template>
  <div class="stay-in-touch w-90">
    <div class="stay-in-touch-container d-flex">
      <div class="stay-in-touch-box d-flex">
        <h5>made for sharing</h5>
        <h2 class="m-05">let's stay in touch</h2>
        <div class="button m-05">
          <a class="btn purple" href=""
            ><i class="fab fa-instagram"></i>follow us</a
          >
        </div>
      </div>
      <div
        v-for="(image, index) in images"
        :key="index"
        class="stay-in-touch-box"
      >
        <img
          :src="require(`../../assets/img/social-${image.img}.jpg`)"
          alt=""
        />
      </div>
    </div>
  </div>
</template>

<script>
export default {
  name: "StayInTouch",
  data() {
    return {
      images: [
        {
          img: "1",
        },
        {
          img: "2",
        },
        {
          img: "3",
        },
        {
          img: "4",
        },
        {
          img: "5",
        },
        {
          img: "6",
        },
      ],
    };
  },
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
      &:nth-of-type(1) {
        flex-basis: calc(100% / 2.04);
        flex-direction: column;
        align-items: center;
        justify-content: center;
        background-color: $lightPurple;
        .fa-instagram {
          margin-right: 0.5em;
        }
      }
      &:nth-of-type(2) {
        order: -1;
      }
    }
  }
}
</style>
