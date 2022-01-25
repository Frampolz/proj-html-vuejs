<template>
  <div class="delivery w-90">
    <div class="delivery-container container-top">
      <div class="filter-box d-flex">
        <div class="delivery-box-left d-flex">
          <h2>tell us how you have in mind</h2>
        </div>
        <div class="delivery-box-right d-flex">
          <div class="box-numb">
            <h5>01</h5>
          </div>
          <div class="details">
            <h5>manual ingredients selection</h5>
            <p>
              Cras consequat lectus vestibulum tortor pulvinar, quis euismod
              nisl varius. Ut eu laoreet ex. Aliquam erat volutpat. Nullam quis
              sagittis nibh, Morbi consectetur ultricies ante ac congue, Donec
              lorem erat, finibus in velit placerat, rutrum
            </p>
          </div>
        </div>
      </div>
    </div>
    <div class="delivery-container container-mid d-flex">
      <div class="delivery-box-left d-flex">
        <div class="filter-box">
          <div class="inner-top d-flex">
            <h2>we start baking</h2>
            <div class="box-numb">
              <h5>02</h5>
            </div>
          </div>
          <div class="inner-bot d-flex">
            <div class="details">
              <h5>sweet &amp; delicious</h5>
              <p>
                Cras consequat lectus vestibulum tortor pulvinar, quis euismod
                nisl varius. Ut eu laoreet ex. Aliquam erat volutpat. Nullam
                quis sagittis nibh, Morbi consectetur ultricies ante ac congue,
                Donec lorem erat, finibus in velit placerat.
              </p>
            </div>
          </div>
        </div>
      </div>
      <div class="delivery-box-right d-flex">
        <div class="details">
          <h5>dont just take our word for it</h5>
          <h2>
            "finally found an alternative to the mass produced products.
            something that incorporates real organic ingrediets, nutrient dense
            wellness while promoting sustainability and activity"
          </h2>
          <h5>rachel cooper, founder</h5>
        </div>
      </div>
    </div>
    <div class="delivery-container container-bot">
      <div class="filter-box d-flex">
        <div class="delivery-box-left d-flex">
          <h2>delivered to yout home</h2>
          <div class="details">
            <h5>baked to order &amp; gift wrapped</h5>
            <p>
              Cras consequat lectus vestibulum tortor pulvinar, quis euismod
              nisl varius. Ut eu laoreet ex. Aliquam erat volutpat. Nullam quis
              sagittis nibh, Morbi consectetur ultricies ante ac congue, Donec
              lorem erat, finibus in velit placerat, rutrum augue.
            </p>
          </div>
        </div>
        <div class="delivery-box-right d-flex">
          <div class="box-numb">
            <h5>03</h5>
          </div>
        </div>
      </div>
    </div>
  </div>
</template>

<script>
export default {
  name: "Delivery",
};
</script>

<style lang="scss">
@import "../../assets/scss/partials/variables.scss";
.delivery {
  margin: 12em;

  .delivery-container {
    width: 100%;
    height: 800px;

    .filter-box {
      width: 100%;
      height: 100%;
      background: linear-gradient(
        180deg,
        rgba(71, 71, 71, 0.2) 0%,
        rgba(0, 0, 0, 0.4) 60%
      );
      flex-direction: row;
    }
  }
  .box-numb {
    h5 {
      font-size: 6em;
      color: white;
    }
  }
  .container-top {
    background-image: url("../../assets/img/bakery-process-1.jpg");
    background-size: cover;

    .delivery-box-left {
      width: 50%;
      padding: 0 5em;
      h2 {
        font-size: 4em;
        color: white;
      }
    }
    .delivery-box-right {
      width: 50%;
      flex-direction: column;
      justify-content: space-between;
      align-items: flex-end;
      padding: 5em;

      .details {
        padding: 0em 3em;
        h5 {
          font-weight: bold;
        }
        p {
          color: white;
          font-size: 1.5em;
          line-height: 1.5em;
        }
      }
    }
  }

  .container-mid {
    margin: 2em 0;
    gap: 2em;

    .delivery-box-left,
    .delivery-box-right {
      width: 50%;
      height: 100%;
    }
    .delivery-box-left {
      background-image: url("../../assets/img/bakery-process-2.jpg");
      background-size: cover;
      background-position: right;
      flex-direction: column;
      justify-content: space-between;
      .inner-top {
        height: 50%;
        justify-content: space-between;
        align-items: baseline;
        padding: 0 4em;
        h2 {
          font-size: 3.5em;
          color: white;
        }
      }
      .inner-bot {
        height: 50%;
        flex-direction: column;
        justify-content: flex-end;
        .details {
          width: 50%;
          padding: 3em 0;
          margin-left: 4em;
          h5 {
            color: lightgray;
          }
          p {
            margin-top: 1em;
            font-size: 1.5em;
            color: white;
          }
        }
      }
    }
    .delivery-box-right {
      background-color: $lightPurple;
      align-items: center;
      .details {
        padding: 3em;
        h2 {
          font-size: 3.5em;
          margin: 1em 0;
        }
      }
    }
  }

  .container-bot {
    background-image: url("../../assets/img/bakery-process-3.jpg");
    background-size: cover;
    background-position: center;
    .delivery-box-left {
      width: 50%;
      flex-direction: column;
      justify-content: space-between;
      padding: 5em;
      h2 {
        color: white;
        font-size: 3.5em;
      }
      .details {
        padding: 0 6em 0 0;
        h5 {
          font-weight: bold;
        }
        p {
          color: white;
          font-size: 1.5em;
          line-height: 1.5em;
          margin-top: 0.5em;
        }
      }
    }
    .delivery-box-right {
      width: 50%;
      justify-content: flex-end;
      .box-numb {
        h5 {
          padding: 1.2em;
        }
      }
    }
  }
}
</style>
