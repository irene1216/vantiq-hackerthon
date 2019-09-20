<template>
  <div class="directory">
    <h1>This is the directory page</h1>
      <div class="mt-3" v-for="lift in lifts">
        <b-card border-variant="info" align="center">
          <b-card-text>Number of floors: {{lift.Floor_Count}}</b-card-text>
          <b-card-text>{{lift.Housing_Estate_Name}}</b-card-text>
          <b-card-text>{{lift.lift_Name}}</b-card-text>
          <b-card-text>{{lift.lift.city}}</b-card-text>
          <b-card-text>{{lift.lift.town}}</b-card-text>

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
      axios.get('https://dev.vantiq.cn/api/v1/resources/custom/BaseInfoForHackathon?token=B__1eBCT0MZJFtJkyS1Y_dcFMcuB8O0Tuc77fKYegqs=').then(response => {
        let array = response.data.slice(0, 10)
        this.formatLocation(array)
      })
    },
    formatLocation(array) {
      console.log("formating")
      console.log(array)
      let tmp = []
      array.forEach((lift)=>{
        lift.city = "Shanghai"
        if (lift.Town_Code === "310114"){
          tmp.push({
            id: lift.id,
            registerId: lift._id,
            building: lift.Housing_Estate_Name,
            floors: lift.Floor_Count,
            city: "Shanghai",
            town: "JiaDing",
            address: lift.lift_Name,
            geo: lift.Lift_Geo
          })
        } else if (lift.Town_Code === "310109") {
          tmp.push({
            id: lift.id,
            registerId: lift._id,
            building: lift.Housing_Estate_Name,
            floors: lift.Floor_Count,
            city: "Shanghai",
            town: "HongKou",
            address: lift.lift_Name,
            geo: lift.Lift_Geo
          })
        }
      })
      this.lifts = tmp
    },
  }
};
</script>

<style scoped>

</style>
