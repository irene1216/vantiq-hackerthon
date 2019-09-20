<template>
  <div class="home">
    <div class="section">
      <Banner/>
    </div>
    <div class="section">
      <PopularBldg/>
    </div>
  </div>
</template>

<script>
// @ is an alias to /src
import HelloWorld from "@/components/HelloWorld.vue";
import Banner from "@/components/Banner.vue";
import PopularBldg from "@/components/PopularBldg";
import axios from 'axios';


export default {
  name: "home",
  components: {
    HelloWorld,
    Banner,
    PopularBldg
  },
  mounted() {
    this.fetchData()
  },
  methods: {
    fetchData() {
      console.log("fetch")
      axios.get('https://dev.vantiq.cn/api/v1/resources/custom/BaseInfoForHackathon?token=B__1eBCT0MZJFtJkyS1Y_dcFMcuB8O0Tuc77fKYegqs=').then(response => {
        console.log(response.data);
      })
    },
  }
};
</script>

<style scoped>
.section{
  height:600px;
}
</style>
