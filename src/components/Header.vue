<template>
  <header id="top" class="header d-flex">
    <div class="header-top d-flex">
      <div class="logo">
        <a href=""><img src="../assets/img/avada-bakery-logo.png" alt="" /></a>
      </div>
      <HeaderMenu />
    </div>
    <div class="header-mid d-flex">
      <div class="header-mid-box d-flex">
        <i class="fas fa-archive"><p>demos</p></i>
      </div>
      <div class="header-mid-box d-flex prize">
        <p><span>$</span> 39</p>
        <h3>on sale</h3>
      </div>
    </div>
    <div class="header-bot d-flex">
      <div class="inner-header-bot">
        <h5>fresh &amp; tasty bakery evert day</h5>
        <h1>the perfect fresh bread</h1>
        <p>
          Cras consequat lectus vestibulum tortor pulvinar, quis euismod nisl
          varius. Aliquam erat volutpat. Nullam quis sagittis nibh ac nulla id
          orci tempor.
        </p>
        <div class="button">
          <a class="btn white" href="">explore our products</a>
        </div>
      </div>
    </div>
  </header>
</template>

<script>
import HeaderMenu from "./header-component/HeaderMenu.vue";
export default {
  name: "Header",
  components: {
    HeaderMenu,
  },
};
</script>

<style lang="scss">
@import "../assets/scss/partials/variables.scss";
.header {
  height: 100vh;
  width: 100%;
  background-image: url("../assets/img/hero-header-bakery.jpg");
  background-size: cover;
  flex-direction: column;
  align-items: center;
  .header-top {
    width: 100%;
    justify-content: space-between;
    padding: 1em;
  }
  .header-mid {
    width: 100%;
    flex-direction: column;
    align-items: flex-end;
    padding: 0 1em;
    position: fixed;
    top: 10em;
    right: 0;
    .header-mid-box {
      width: 70px;
      height: 70px;
      justify-content: center;
      align-items: center;
      text-align: center;
      border-radius: 8px;
      background-color: white;
      box-shadow: 4px 0px 15px lightgray;
      &:first-of-type {
        margin-bottom: 0.5em;
      }
      .fa-archive {
        font-size: 1.5em;
        p {
          font-size: 0.6em;
          font-weight: normal;
          text-transform: capitalize;
        }
      }
    }
    .prize {
      flex-direction: column;
      p {
        color: $green;
        font-size: 1.5em;
        font-weight: bold;
        span {
          vertical-align: super;
        }
      }
      h3 {
        font-size: 0.9em;
        font-weight: normal;
        text-transform: capitalize;
      }
    }
  }
  .header-bot {
    height: 80%;
    width: 90%;
    padding: 10em 0;
    .inner-header-bot {
      width: 30%;
      h1 {
        font-size: 3.5em;
        margin: 0.2em 0em;
        text-transform: capitalize;
        color: $purple;
      }

      p {
        font-size: 1.2em;
        line-height: 1.5em;
        color: $lightGrey;
      }
    }
  }
}
</style>
