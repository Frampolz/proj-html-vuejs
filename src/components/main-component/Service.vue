<template>
  <div class="service w-90 d-flex">
    <div class="heading">
      <h5>corporate &amp; weddings</h5>
      <h2>baking special moment</h2>
    </div>
    <div class="service-box-container d-flex">
      <div class="service-box">
        <img class="corporate" src="../../assets/img/corporate-bg.jpg" alt="" />
        <img
          class="hover-corporate"
          src="../../assets/img/corporate-hover-bg.jpg"
          alt=""
        />
        <div class="hover-service-box">
          <h5>international bakery</h5>
          <h2>corporate event</h2>
          <div class="button">
            <a class="btn purple" href="">explore more</a>
          </div>
        </div>
      </div>
      <div class="service-box">
        <img class="wedding" src="../../assets/img/wedding-bg.jpg" alt="" />
        <img
          class="hover-wedding"
          src="../../assets/img/wedding-hover-bg.jpg"
          alt=""
        />
        <div class="hover-service-box">
          <h5>private dining hall</h5>
          <h2>wedding &amp; parties</h2>
          <div class="button">
            <a class="btn purple" href="">explore more</a>
          </div>
        </div>
      </div>
    </div>
  </div>
</template>

<script>
export default {
  name: "Service",
  data() {
    return {
      serviceData: [
        {
          image: ''
        },
      ]
    }
  }
};
</script>

<style lang="scss">
.service {
  margin-top: 12em;
  flex-direction: column;
  .heading {
    text-align: center;
    h2 {
      text-transform: capitalize;
    }
  }
  .service-box-container {
    gap: 8em;
    .service-box {
      flex-basis: calc(100% / 2);
      position: relative;

      &:hover .hover-corporate,
      &:hover .hover-wedding,
      &:hover .hover-service-box {
        display: block;
      }
      &:hover .corporate,
      &:hover .wedding {
        display: none;
      }
      img {
        width: 100%;
        border-radius: 4px;
      }
      .hover-corporate,
      .hover-wedding {
        display: none;
      }
      .hover-service-box {
        display: none;
        position: absolute;
        top: 50%;
        left: 50%;
        transform: translate(-50%, -50%);
        h2 {
          color: white;
          text-transform: capitalize;
          font-size: 2.5em;
        }
        h5 {
          text-align: center;
          color: white;
        }
        .button {
          display: flex;
          justify-content: center;
          a {
            color: white;
          }
        }
      }
    }
  }
}
</style>
