<template>
  <header class="header d-flex">
    <div class="header-top d-flex">
      <div class="logo">
        <img src="../assets/img/avada-bakery-logo.png" alt="" />
      </div>
      <HeaderMenu />
    </div>
    <div class="header-bot d-flex">
      <div class="inner-header-bot">
        <h2>fresh &amp; tasty bakery evert day</h2>
        <h1>the perfect fresh bread</h1>
        <p>
          Cras consequat lectus vestibulum tortor pulvinar, quis euismod nisl
          varius. Aliquam erat volutpat. Nullam quis sagittis nibh ac nulla id
          orci tempor.
        </p>
        <div class="button"><a href="">explore our products</a></div>
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
  .header-bot {
    height: 80%;
    width: 90%;
    align-items: center;
    .inner-header-bot {
      width: 30%;
      h1 {
        font-size: 3.5em;
        margin: 0.2em 0em;
        text-transform: capitalize;
        color: $purple;
      }
      h2 {
        font-size: 0.8em;
        font-weight: normal;
        text-transform: uppercase;
        color: $lightGrey;
      }
      p {
        font-size: 1.2em;
        line-height: 1.5em;
        color: $lightGrey;
      }
      .button {
        display: inline-block;
        margin-top: 2em;
        a {
          padding: 0.7em 1.7em;
          border-radius: 5px;
          background-color: white;
          font-size: 1.1em;
          color: $purple;
        }
      }
    }
  }
}
</style>
