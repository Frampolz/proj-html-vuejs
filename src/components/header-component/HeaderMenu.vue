<template>
  <ul class="menu d-flex">
    <li>
      <a href="">home</a>
    </li>
    <li>
      <a href="">shop</a>
    </li>
    <li>
      <a href="">about</a>
    </li>
    <li>
      <a href="">gallery</a>
    </li>
    <li>
      <a href="">locations</a>
    </li>
    <li>
      <a href="">jouenal</a>
    </li>
    <li>
      <a href="">contact</a>
    </li>
    <li>
      <a href=""> my account</a>
    </li>
    <li>
      <a href=""><i class="fas fa-shopping-cart"></i></a>
    </li>
  </ul>
</template>

<script>
export default {
  name: "HeaderMenu",
};
</script>

<style lang="scss">
@import "../../assets/scss/partials/variables.scss";

.menu {
  align-items: center;

  li {
    margin-right: 2.5em;
    a {
      text-transform: uppercase;
      font-size: 0.8em;
    }
  }
}
</style>
