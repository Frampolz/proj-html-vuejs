<template>
  <ul class="menu d-flex">
    <li v-for="(link, index) in links" :key="index">
      <a
        @click="select(index)"
        :class="link.index == true ? 'selected' : ''"
        href="#"
        >{{ link.link }}</a
      >
    </li>
    <li>
      <a href=""><i class="fas fa-shopping-cart"></i></a>
    </li>
  </ul>
</template>

<script>
export default {
  name: "HeaderMenu",
  data() {
    return {
      links: [
        {
          link: "home",
          index: true,
        },
        {
          link: "shop",
          index: false,
        },
        {
          link: "about",
          index: false,
        },
        {
          link: "gallery",
          index: false,
        },
        {
          link: "locations",
          index: false,
        },
        {
          link: "journal",
          index: false,
        },
        {
          link: "contact",
          index: false,
        },
        {
          link: "my account",
          index: false,
        },
      ],
    };
  },
  methods: {
    select(index) {
      this.links.forEach((element, indexlink) => {
        if (indexlink == index) {
          element.index = true;
        } else {
          element.index = false;
        }
      });
    },
  },
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
      padding-bottom: 5px;
      &:hover,
      &:active,
      &:focus {
        border-bottom: 2px solid $purple;
      }
    }
  }
  .selected {
    border-bottom: 2px solid $purple;
  }
}
</style>
