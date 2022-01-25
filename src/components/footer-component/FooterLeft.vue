<template>
  <div class="footer-left">
    <div class="logo">
      <img src="../../assets/img/avada-bakery-logo-retina-200x97.png" alt="" />
    </div>
    <div class="footer-menu">
      <ul>
        <li><a href="">shop</a></li>
        <li><a href="">about</a></li>
        <li><a href="">gallery</a></li>
        <li><a href="">locations</a></li>
        <li><a href="">journal</a></li>
        <li><a href="">contact</a></li>
        <li><a href="">orders</a></li>
        <li>
          <a href=""><i class="fas fa-shopping-cart"></i><span>0</span></a>
        </li>
      </ul>
    </div>
    <div class="copyright">
      <h6>
        &copy; copyright 2012 - 2020 | avada theme by themeFusion | all rights
        reserved | powered by wordPress
      </h6>
    </div>
  </div>
</template>

<script>
export default {
  name: "FooterLeft",
};
</script>

<style lang="scss">
@import "../../assets/scss/partials/variables.scss";
.footer-menu {
  ul {
    li {
      margin: 2em 3.5em 8em 0;
      a {
        text-transform: capitalize;
        font-size: 1.2em;
        .fa-shopping-cart {
          margin-right: 0.5em;
          font-size: 0.8em;
        }
        span {
          background-color: $lightPurple;
          padding: 4px 10px;
          border-radius: 50%;
        }
      }
    }
  }
}
.copyright {
  h6 {
    font-size: 0.8em;
    color: grey;
    text-transform: capitalize;
  }
}
</style>
