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

export default {
  name: "home",
  components: {
    HelloWorld,
    Banner,
    PopularBldg
  }
};
</script>

<style scoped>
.section{
  height:600px;
  margin-bottom: 5%;
}
</style>
