<template>
  <div class="shop d-flex">
    <div class="inner-shop">
      <h5>try our seasonal products</h5>
      <h2 class="mt-05">Order for pick-up or delivery to your home</h2>
      <div class="button">
        <a class="btn white" href="">shop now</a>
      </div>
    </div>
  </div>
</template>

<script>
export default {
  name: "Shop",
};
</script>

<style lang="scss">
.shop {
  width: 100%;
  margin-top: 10em;
  background-image: url("../../assets/img/call-to-action-bg.jpg");
  background-size: 130em;
  background-position: top right;
  background-repeat: no-repeat;
  justify-content: center;
  .inner-shop {
    width: 60%;
    margin: 4em 0;
    h2 {
      color: white;
      font-size: 3.5em;
      padding: 0 4em 0 0;
    }

    .white {
      color: black;
    }
  }
}
</style>
