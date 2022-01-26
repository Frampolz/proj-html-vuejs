<template>
  <div class="all-product d-flex">
    <div class="all-product-container w-90 d-flex">
      <div class="all-product-box heading d-flex">
        <h2>Find a freshly baked product perfet for you</h2>
        <h5>
          Integer a nibh vitae ex porttitor rutrum et ut velit. Etiam ac felis
          at leo feugiat placerat. Sed ac nulla id orci tempor convallis sed.
        </h5>
        <div class="button">
          <a class="btn purple" href="">shopping all products</a>
        </div>
      </div>
      <div class="all-product-box d-flex">
        <img
          :src="
            require(`../../assets/img/${productArray[counter].image}-400x510.jpg`)
          "
          alt=""
        />

        <div class="filter">
          <h5>select options / quick view</h5>
        </div>
        <h3>{{ productArray[counter].item }}</h3>
        <p>{{ productArray[counter].prize }}</p>
        <div @click="prev()" class="left-arrow">
          <i class="fas fa-chevron-left"></i>
        </div>
      </div>
      <div class="all-product-box d-flex">
        <img
          :src="
            require(`../../assets/img/${productArray[counter1].image}-400x510.jpg`)
          "
          alt=""
        />
        <div class="filter">
          <h5>select options / quick view</h5>
        </div>
        <h3>{{ productArray[counter1].item }}</h3>
        <p>{{ productArray[counter1].prize }}</p>
      </div>
      <div class="all-product-box d-flex">
        <img
          :src="
            require(`../../assets/img/${productArray[counter2].image}-400x510.jpg`)
          "
          alt=""
        />
        <div class="filter">
          <h5>select options / quick view</h5>
        </div>
        <h3>{{ productArray[counter2].item }}</h3>
        <p>{{ productArray[counter2].prize }}</p>
      </div>
      <div class="all-product-box d-flex">
        <img
          :src="
            require(`../../assets/img/${productArray[counter3].image}-400x510.jpg`)
          "
          alt=""
        />
        <div class="filter">
          <h5>select options / quick view</h5>
        </div>
        <h3>{{ productArray[counter3].item }}</h3>
        <p>{{ productArray[counter3].prize }}</p>
        <div @click="next()" class="right-arrow">
          <i class="fas fa-chevron-right"></i>
        </div>
      </div>
    </div>
  </div>
</template>

<script>
export default {
  name: "AllProd",
  data() {
    return {
      counter: 0,
      counter1: 1,
      counter2: 2,
      counter3: 3,
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
      this.counter == index;
      this.counter -= 1;
      if (this.counter < 0) {
        this.counter = this.productArray.length - 1;
      }
      this.counter1 == index;
      this.counter1 -= 1;
      if (this.counter1 < 0) {
        this.counter1 = this.productArray.length - 1;
      }
      this.counter2 == index;
      this.counter2 -= 1;
      if (this.counter2 < 0) {
        this.counter2 = this.productArray.length - 1;
      }
      this.counter3 == index;
      this.counter3 -= 1;
      if (this.counter3 < 0) {
        this.counter3 = this.productArray.length - 1;
      }
    },
    next(index) {
      this.counter == index;
      this.counter++;
      if (this.counter > this.productArray.length - 1) {
        this.counter = 0;
      }
      this.counter1 == index;
      this.counter1++;
      if (this.counter1 > this.productArray.length - 1) {
        this.counter1 = 0;
      }
      this.counter2 == index;
      this.counter2++;
      if (this.counter2 > this.productArray.length - 1) {
        this.counter2 = 0;
      }
      this.counter3 == index;
      this.counter3++;
      if (this.counter3 > this.productArray.length - 1) {
        this.counter3 = 0;
      }
    },
  },
  created() {},
};
</script>

<style lang="scss">
.all-product {
  margin-top: 12em;
  .heading {
    h5 {
      line-height: 2em;
    }
  }
  .all-product-container {
    margin: auto;
    gap: 1.5em;

    .all-product-box {
      flex-basis: calc(100% / 5);
      height: 500px;
      position: relative;
      text-align: center;
      flex-direction: column;
      justify-content: center;
      .filter {
        display: none;
        width: 100%;
        height: 80%;
        position: absolute;
        top: 0;
        left: 0;
        z-index: 2;
      }
      &:hover .filter {
        display: flex;
        justify-content: center;
        align-items: center;
        background-color: rgba(0, 0, 0, 0.5);
        h5 {
          cursor: pointer;
          color: white;
        }
      }
      h3 {
        margin: 1em;
        font-size: 1.4em;
      }
      p {
        font-size: 1.2em;
      }
      img {
        width: 100%;
        height: 100%;
        object-fit: cover;
      }
    }
  }
}
</style>
