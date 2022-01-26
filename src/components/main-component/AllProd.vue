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
      <div
        v-for="(counter, index) in counters"
        :key="index"
        class="all-product-box d-flex"
      >
        <img
          :src="
            require(`../../assets/img/${
              productArray[counter.counter].image
            }-400x510.jpg`)
          "
          alt=""
        />
        <div class="filter">
          <h5>select options / quick view</h5>
        </div>
        <h3>{{ productArray[counter.counter].item }}</h3>
        <p>{{ productArray[counter.counter].prize }}</p>
        <div @click="prev()" class="left-arrow">
          <i class="fas fa-chevron-left"></i>
        </div>
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
      counters: [
        {
          counter: 0,
        },
        {
          counter: 1,
        },
        {
          counter: 2,
        },
        {
          counter: 3,
        },
      ],
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
      this.counters.forEach((element, countIndex) => {
        countIndex == index;
        element.counter == countIndex;
        element.counter--;

        if (element.counter < 0) {
          element.counter = this.productArray.length - 1;
        }
      });
    },
    next(index) {
      this.counters.forEach((element, countIndex) => {
        countIndex == index;
        element.counter == countIndex;
        element.counter++;

        if (element.counter > this.productArray.length - 1) {
          element.counter = 0;
        }
      });
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
      &:nth-of-type(3),
      &:nth-of-type(4) {
        .left-arrow,
        .right-arrow {
          display: none;
        }
      }
      &:nth-of-type(2) {
        .right-arrow {
          display: none;
        }
      }
      &:nth-of-type(5) {
        .left-arrow {
          display: none;
        }
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
