<template>
  <div id="app">
    <div id="nav">
      <router-link to="/"><h1 style="text-decoration: none;"><strong style="text-decoration: none;">UpLift</strong></h1></router-link>
    </div>
    <router-view />
  </div>
</template>


<style>


@import url('https://fonts.googleapis.com/css?family=Niramit:700|Roboto|Staatliches&display=swap');

body {
  margin:0;
}

h1{
  color:black;
}

#app {
  font-family: "Avenir", Helvetica, Arial, sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  text-align: center;
  color: #2c3e50;
}

#nav {
  padding: 30px;
}

#nav a {
  font-weight: bold;
  color: #2c3e50;
}

#nav a.router-link-exact-active {
  color: #42b983;
}
</style>
