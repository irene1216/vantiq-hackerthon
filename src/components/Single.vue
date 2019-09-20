<template>
  <div class="single-wrapper">
    <!-- building info goes here -->
    <div class="card-all">
      <div class="container">
        <div class="row">
          <div class="col-sm-12">
            <div class="card-single shadow-sm p-2 mt-4">
              <div class="card-wrapper d-flex">
                <div class="card-half flex-grow-1">
                  <area-chart :data="{'2019-09-01 00:00:00 -0800': 120, '2019-09-15 00:01:00 -0800': 367, '2019-09-30 00:01:00 -0800': 475}"></area-chart>
                </div>
                <div class="card-half flex-grow-1 p-4">
                  <h2>Lift #1</h2>
                  <p>Ad space: 30 * 20 * 30</p>
                  <p>Peak time: 11:00 - 14:00</p>
                  <p>Foot traffic: 26347 monthly</p>
                  <a href="#" class="btn btn-primary">Reserve an ad space</a>
                </div>
              </div>
            </div>
            <div class="card-single shadow-sm p-2 mt-4">
              <div class="card-wrapper d-flex">
                <div class="card-half flex-grow-1">
                  <area-chart :data="{'2019-09-01 00:00:00 -0800': 59, '2019-09-15 00:01:00 -0800': 128, '2019-09-30 00:01:00 -0800': 530}"></area-chart>
                </div>
                <div class="card-half flex-grow-1 p-4">
                  <h2>Lift #2</h2>
                  <p>Ad space: 30 * 50 * 60</p>
                  <p>Peak time: 15:00 - 18:00</p>
                  <p>Foot traffic: 34758 monthly</p>
                  <a href="#" class="btn btn-primary">Reserve an ad space</a>
                </div>
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
  name: "Single",
  components: {
  }
};
</script>

<style scoped>
  .card-single {
    background: #fff;
    text-align: left;
  }
  .card-half {
    width: 50%;
    display: inline-block;
  }

</style>
