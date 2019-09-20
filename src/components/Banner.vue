<template>
  <div class="banner">
    <div class="container">
      <h1><strong>Uplift & Elevate<br>Your Marketing Strategy</strong></h1>
      <div class="search d-flex space-between">
      <b-form-input v-model="text" placeholder="Enter your name"></b-form-input>
      <b-dropdown  class="ml-1" text="District" variant="primary">
        <b-dropdown-item>JiaDing </b-dropdown-item>
        <b-dropdown-item>Hongkou</b-dropdown-item>
      </b-dropdown>
      <b-dropdown class="ml-1" text="Category" variant="primary">
        <b-dropdown-item>a</b-dropdown-item>
        <b-dropdown-item>b</b-dropdown-item>
        <b-dropdown-item>c</b-dropdown-item>
      </b-dropdown>
      </div>

    </div>
  </div>
</template>

<script>
  export default {
    name: "Banner",
    data() {
      return{
        text:''
      }
    }
  };
</script>

<style scoped>

h1{
  font-size: 60px;
  color:white;
  text-shadow: 0px 0px 2px #888888;
}

.search{
  padding-top: 2%;
  width:100%;
  justify-content: center;

}

.search input{
  width:60%;
}


.banner{
  padding-top: 200px;
  padding-bottom: 200px;
  object-fit: cover;
  background: url("https://images.unsplash.com/photo-1554283329-071a1ca2caef?ixlib=rb-1.2.1&ixid=eyJhcHBfaWQiOjEyMDd9&auto=format&fit=crop&w=934&q=80");
  background-repeat: no-repeat;
  background-position: center;
  background-size: cover;
}

</style>
