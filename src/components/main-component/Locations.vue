<template>
  <div class="location d-flex w-90">
    <div class="heading">
      <h5>Locations</h5>
      <h2>visit our bakeries</h2>
    </div>
    <div class="locations-box-container d-flex">
      <div class="location-box-left">
        <img src="../../assets/img/new-york-bk.jpg" alt="" />
        <div class="location">
          <h2>new york</h2>
          <div class="location-details d-flex">
            <div class="phone">
              <h5>call us</h5>
              <p>1.800.458.556</p>
            </div>
            <div class="business-hour">
              <h5>open all week</h5>
              <p>9:00 AM - 6:00 PM</p>
            </div>
            <div class="maps">
              <div class="button m-0">
                <a class="btn white" href="">view map</a>
              </div>
            </div>
          </div>
        </div>
      </div>
      <div class="location-box-right">
        <img src="../../assets/img/london-bk.jpg" alt="" />
        <div class="location">
          <h2>london</h2>
          <div class="location-details d-flex">
            <div class="phone">
              <h5>call us</h5>
              <p>1.800.458.556</p>
            </div>
            <div class="business-hour">
              <h5>open all week</h5>
              <p>9:00 AM - 6:00 PM</p>
            </div>
            <div class="maps">
              <div class="button m-0">
                <a class="btn white" href="">view map</a>
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
    .location-box-left {
      background-color: $atoll;
    }
    .location-box-right {
      background-color: $chalky;
    }
    .location-box-left,
    .location-box-right {
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
