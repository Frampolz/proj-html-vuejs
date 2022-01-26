<template>
  <div class="our-prod w-90 d-flex">
    <div class="our-prod-box">
      <div class="inner-our-prod-box">
        <h5>our products</h5>
        <h2>
          All our delectable pastries are backed fresh in our Kitchen very
          morning, and are made with all- natural, all organic ingredients.
        </h2>
        <div class="button">
          <a class="purple btn" href="">start shopping</a>
        </div>
      </div>
    </div>
    <div class="our-prod-box">
      <div @click="prev()" class="left-arrow">
        <i class="fas fa-chevron-left"></i>
      </div>
      <img
        :src="require(`../../assets/img/${productArray[counter].image}.jpg`)"
        alt=""
      />
      <div class="filter">
        <div class="prod-details">
          <h3>{{ productArray[counter].item }}</h3>
          <h6>{{ productArray[counter].category }}</h6>
          <h3>{{ productArray[counter].prize }}</h3>
        </div>
      </div>
    </div>

    <div class="our-prod-box">
      <div @click="next()" class="right-arrow">
        <i class="fas fa-chevron-right"></i>
      </div>
      <img
        :src="require(`../../assets/img/${productArray[counter1].image}.jpg`)"
        alt=""
      />
      <div class="filter">
        <div class="prod-details">
          <h3>{{ productArray[counter1].item }}</h3>
          <h6>{{ productArray[counter1].category }}</h6>
          <h3>{{ productArray[counter1].prize }}</h3>
        </div>
      </div>
    </div>
  </div>
</template>

<script>
export default {
  name: "OurProd",
  data() {
    return {
      counter: 0,
      counter1: 1,
    };
  },
  props: {
    productArray: {
      type: Array,
      default() {
        return [];
      },
    },
  },
  methods: {
    prev(index) {
      this.counter1 == index;
      this.counter1 -= 1;
      if (this.counter1 < 0) {
        this.counter1 = this.productArray.length - 1;
      }
      this.counter == index;
      this.counter -= 1;
      if (this.counter < 0) {
        this.counter = this.productArray.length - 1;
      }
    },
    next(index) {
      this.counter1 == index;
      this.counter1++;
      if (this.counter1 > this.productArray.length - 1) {
        this.counter1 = 0;
      }
      this.counter == index;
      this.counter++;
      if (this.counter > this.productArray.length - 1) {
        this.counter = 0;
      }
    },
  },
  created() {},
};
</script>

<style lang="scss">
@import "../../assets/scss/partials/variables.scss";
.our-prod {
  gap: 1em;
  .our-prod-box {
    flex-basis: calc(100% / 3);
    position: relative;
    .filter {
      width: 100%;
      height: 100%;
      position: absolute;
      top: 0;
      left: 0;
      z-index: 3;
    }
    img {
      width: 100%;
    }
    &:hover .prod-details {
      display: block;
    }
    &:hover .filter {
      background-color: rgba(0, 0, 0, 0.5);
    }

    .prod-details {
      display: none;
      position: absolute;
      top: 50%;
      left: 50%;
      transform: translate(-50%, -50%);
      h3,
      h6 {
        color: white;
        text-align: center;
      }
      h6 {
        margin: 1em 0;
        font-size: 1em;
        font-weight: normal;
      }
    }
  }
  .inner-our-prod-box {
    h2 {
      padding-right: 3em;
    }
  }
}
</style>
