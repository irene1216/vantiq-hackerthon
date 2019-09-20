<template>
  <div class="banner">
    <div class="container">
    <div class="search">
      <b-input-group v-for="size in ['lg']" :key="size" :size="size"class="mb-3">
        <b-form-input></b-form-input>
        <b-input-group-append>
          <b-button size="sm" text="Search" variant="dark">Button</b-button>
        </b-input-group-append>
      </b-input-group>
    </div>
    </div>
  </div>
</template>

<script>
  export default {
    name: "Banner",
    props: {
    }
  };
</script>

<style scoped>
.search{
  width:100%;
}

.search input{
  width:40%;
}

.banner{
  padding-top: 300px;
  padding-bottom: 300px;
  background: url("http://www.liftupmarketing.in/wp-content/uploads/2018/10/fd206442097621.57c0375096cae.jpg");
}
</style>
