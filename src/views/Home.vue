<template>
  <div class="home">
      <Banner/>

    <div class="section">
      <Directory/>
    </div>

  </div>
</template>

<script>
// @ is an alias to /src
import HelloWorld from "@/components/HelloWorld.vue";
import Banner from "@/components/Banner.vue";
import Directory from "@/components/Directory.vue";
import axios from 'axios';


export default {
  name: "home",
  components: {
    HelloWorld,
    Banner,
    Directory
  },
  mounted() {
    this.fetchData()
  },
  data(){
    return {
      activeID: null,
      selectedLift: {},
      lifts: {}
    }
  },
  methods: {
    fetchData() {
      axios.get('https://dev.vantiq.cn/api/v1/resources/custom/BaseInfoForHackathon?token=B__1eBCT0MZJFtJkyS1Y_dcFMcuB8O0Tuc77fKYegqs=').then(response => {
        this.lifts = response.data.slice(0, 10)
      })
    },

  }
};
</script>

<style scoped>

</style>
