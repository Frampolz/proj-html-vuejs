<template>
  <div class="footer-right d-flex">
    <div class="newsletter">
      <h2>Subscribe to our Newsletter</h2>
      <div class="input">
        <input type="text" placeholder="Enter email address*" />
        <div class="button">
          <a class="btn purple" href="">Subscribe</a>
        </div>
      </div>
    </div>
    <div class="social-link">
      <a v-for="(social, index) in socialLink" :key="index" href="#"
        ><i :class="social.link"></i
      ></a>
    </div>
  </div>
</template>

<script>
export default {
  name: "FooterRight",
  data() {
    return {
      socialLink: [
        {
          link: "fab fa-instagram",
        },
        {
          link: "fab fa-twitter",
        },
        {
          link: "fab fa-facebook-f",
        },
        {
          link: "fab fa-pinterest-p",
        },
      ],
    };
  },
};
</script>

<style lang="scss">
@import "../../assets/scss/partials/variables.scss";
.footer-right {
  width: 47%;
  flex-direction: column;
  align-items: flex-end;
  justify-content: space-between;
  .newsletter {
    h2 {
      font-size: 1.5em;
      text-align: right;
    }
    input {
      margin-right: 1em;
      padding: 0.7em 15em 0.7em 1em;
      border-radius: 5px;
      border: 1px solid lightgray;
      outline: none;
      font-size: 1em;
    }
  }
  .social-link {
    a {
      margin: 1.5em;
    }
  }
}
</style>
