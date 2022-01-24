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
        <img src="../../assets/img/choco-chip-cookies-400x510.jpg" alt="" />
        <h3>choco chip cookies</h3>
        <p>$19.00- $39.00</p>
        <div class="left-arrow">
          <i class="fas fa-chevron-left"></i>
        </div>
      </div>
      <div class="all-product-box d-flex">
        <img src="../../assets/img/strawberry-jam-cookies-400x510.jpg" alt="" />
        <h3>strawberry jam cookies</h3>
        <p>$24.00- $62.00</p>
      </div>
      <div class="all-product-box d-flex">
        <img src="../../assets/img/strawberry-donut-400x510.jpg" alt="" />
        <h3>strawberry donut</h3>
        <p>$24.00- $42.00</p>
      </div>
      <div class="all-product-box d-flex">
        <img src="../../assets/img/perfect-macarons-400x510.jpg" alt="" />
        <h3>perfect macarons</h3>
        <p>$18.00- $52.00</p>
        <div class="right-arrow">
          <i class="fas fa-chevron-right"></i>
        </div>
      </div>
    </div>
  </div>
</template>

<script>
export default {
  name: "AllProd",
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
      h3 {
        margin: 1em;
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
