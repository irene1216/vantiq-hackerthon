<template>
  <div class="single-page">
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

<style scoped>
  .single-page {
    background: #f8f8f8;
    height: 100vh;
  }
</style>
