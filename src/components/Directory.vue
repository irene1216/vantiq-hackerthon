<template>
  <div class="directory">
    <h1>This is the directory page</h1>
      <div class="mt-3" v-for="lift in lifts">
        <b-card border-variant="info" align="center">
          <b-card-text>Number of floors: {{lift.Floor_Count}}</b-card-text>
          <b-card-text>{{lift.Housing_Estate_Name}}</b-card-text>
          <b-card-text>{{lift.lift_Name}}</b-card-text>
          <b-card-text>{{lift.Lift_Provider_Code}}</b-card-text>

        </b-card>
      </div>
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
      console.log("in directory")
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
