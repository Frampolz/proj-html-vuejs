<template>
  <div class="location d-flex w-90">
    <div class="heading">
      <h5>Locations</h5>
      <h2>visit our bakeries</h2>
    </div>
    <div class="locations-box-container d-flex">
      <div
        v-for="(location, index) in locations"
        :key="index"
        :style="`background-color: ${location.color}`"
        class="location-box"
      >
        <img
          :src="require(`../../assets/img/${location.image}-bk.jpg`)"
          alt=""
        />
        <div class="location">
          <h2>{{ location.city }}</h2>
          <div class="location-details d-flex">
            <div class="phone">
              <h5>{{ location.phone }}</h5>
              <p>{{ location.number }}</p>
            </div>
            <div class="business-hour">
              <h5>{{ location.opening }}</h5>
              <p>{{ location.hours }}</p>
            </div>
            <div class="maps">
              <div class="button m-0">
                <a class="btn white" href="">{{ location.maps }}</a>
              </div>
            </div>
          </div>
        </div>
      </div>
    </div>
  </div>
</template>

<script>
export default {
  name: "Locations",
  data() {
    return {
      locations: [
        {
          city: "new york",
          image: "new-york",
          phone: "call us",
          number: "1.800.458.556",
          opening: "open all week",
          hours: "9:00 AM - 6:00 PM",
          maps: "View map",
          color: "rgba(8, 104, 117,0.1)",
        },
        {
          city: "london",
          image: "london",
          phone: "call us",
          number: "1.800.458.556",
          opening: "open all week",
          hours: "9:00 AM - 6:00 PM",
          maps: "View map",
          color: "rgba(240, 202, 161, 0.3)",
        },
      ],
    };
  },
};
</script>

<style lang="scss">
@import "../../assets/scss/partials/variables.scss";
.location {
  flex-direction: column;
  align-items: center;
  .heading {
    text-align: center;
  }
  .locations-box-container {
    .location-box {
      width: 50%;
      img {
        width: 100%;
      }
      .location {
        margin-bottom: 2em;
        h2 {
          text-align: center;
          text-transform: capitalize;
        }
        .location-details {
          justify-content: space-around;
          .phone,
          .business-hour,
          .maps {
            text-align: center;
          }
          h5 {
            margin-bottom: 0.5em;
          }
          p {
            color: grey;
          }
        }
      }
    }
  }
}
</style>
