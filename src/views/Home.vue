<template>
  <div class="home">
    <div class="section">
      <Banner/>
    </div>
    <div class="section">
      <PopularBldg/>
    </div>
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

export default {
  name: "home",
  components: {
    HelloWorld,
    Banner,
    Directory
  }
};
</script>

<style scoped>
.section {
  height: 600px;
}
</style>
