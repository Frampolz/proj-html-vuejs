<template>
  <div class="footer-left">
    <div class="logo">
      <img src="../../assets/img/avada-bakery-logo-retina-200x97.png" alt="" />
    </div>
    <div class="footer-menu">
      <ul>
        <li v-for="(link, index) in menuLink" :key="index">
          <a href="#">{{ link.link }}</a>
        </li>
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
  data() {
    return {
      menuLink: [
        {
          link: "shop",
        },
        {
          link: "about",
        },
        {
          link: "gallery",
        },
        {
          link: "locations",
        },
        {
          link: "journal",
        },
        {
          link: "contact",
        },
        {
          link: "orders",
        },
      ],
    };
  },
};
</script>

<style lang="scss">
@import "../../assets/scss/partials/variables.scss";
.footer-menu {
  ul {
    li {
      margin: 2em 3em 8em 0;
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
