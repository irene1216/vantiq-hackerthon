<template>
  <div class="directory">
    <h1>This is the directory page</h1>
      <b-card border-variant="info" header="Info" align="center">
        <b-card-text>Lorem ipsum dolor sit amet, consectetur adipiscing elit.</b-card-text>
      </b-card>
  </div>
</template>

<script>
import axios from 'axios';

export default {
  name: "Directory",
  components: {

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
      console.log("fetch")
      axios.get('https://dev.vantiq.cn/api/v1/resources/custom/BaseInfoForHackathon?token=B__1eBCT0MZJFtJkyS1Y_dcFMcuB8O0Tuc77fKYegqs=').then(response => {
        console.log(response.data.slice(0, 10));
        this.lifts = response.data.slice(0, 10)
      })
    },
  }
};
</script>

<style scoped>

</style>
