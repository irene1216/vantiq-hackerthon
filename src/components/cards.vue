<template>
  <div class="main">
      <b-card border-variant="info" header="Info" align="center">
        <b-card-text>Lorem ipsum dolor sit amet, consectetur adipiscing elit.</b-card-text>
      </b-card>
  </div>
</template>
<script>
export default {
  name: "Cards",
  props: {
    buildingName: String,
    floors: Number,
    City: String,
    District: String,
    liftsNo: Number
  }
}
</script>
<style>

</style>
