<template>
  <div class="about">
    <div class="container d-flex p-4">
      <div class="col-6 text-left">
        <h1>绿地新江桥城299弄</h1>
        <p><strong>地址：</strong>金耀南路299弄12-1-1</p>
        <p><strong>分類：</strong>住宅</p>
        <p class="mt-3">绿地集团表示，江桥基地项目将由北至南逐次开发，项目在首期2009年6月24日开工后全力加快项目推进，计划在8月份再开工12万平方米，以后每月开工一批，年内实现全部开工。力争明2010年竣工18万平方米，同时按照需求作适当灵活调节，到2011年6月实现整个社区基本竣工</p>
      </div>
      <div class="slider">
        <b-carousel
          id="carousel-1"
          v-model="slide"
          :interval="4000"
          controls
          indicators
          img-width="1024"
          img-height="1000"
          style="text-shadow: 1px 1px 2px #333;"
          @sliding-start="onSlideStart"
          @sliding-end="onSlideEnd"
        >
        <b-carousel-slide
          img-src="https://img.kinpan.com/Files/kinpanto/%E4%B8%8A%E6%B5%B7%E7%BB%BF%E5%9C%B0%E6%96%B0%E6%B1%9F%E6%A1%A5%E5%9F%8E/160108105956465.jpg"
        ></b-carousel-slide>
        <b-carousel-slide
          img-src="http://alltypeselevators.com/site/wp-content/uploads/2013/08/elevators.jpg"
        ></b-carousel-slide>
        <b-carousel-slide
          img-src="https://www.forms-surfaces.com/sites/default/files/imagecache/gal-reg-2x/images/6.1_NR_6687_07152015.jpg"
        ></b-carousel-slide>
        </b-carousel>
      </div>
    </div>
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
    },
    data() {
      return {
        slide: 0,
        sliding: null
      }
    },
    methods: {
      onSlideStart(slide) {
        this.sliding = true
      },
      onSlideEnd(slide) {
        this.sliding = false
      }
    }
  }
</script>

<style scoped>
  .about {
    height: 100vh;
    background: #f2f2f2;
  }

  p {
    margin-bottom: 0;
  }

  .single-page {
    background: #f8f8f8;
    height: 100vh;
  }

  .about {
    height: 300px;
  }

  .carousel {
    height: 100%;
  }

  .carousel-item {
    height: 100%;
  }
</style>
