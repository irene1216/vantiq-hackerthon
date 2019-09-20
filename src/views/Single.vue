<template>
  <div class="single-page">
    <div>
      <div class="single-infos">
        <h2>Biulding name</h2>
        <p>Building location</p>
        <p><strong>catogery</strong></p>
      </div>
      <div class="slider">
      </div>
    </div>
    <Single/>
  </div>
</template>
<script>
import Single from "@/components/Single.vue";

export default {
  name: "single",
    components: {
    Single
  },
}
</script>
