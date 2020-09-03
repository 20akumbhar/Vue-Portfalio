<template>
  <div id="app">
    <Navbar />
    <br />
    <br />
    <home/>
    <Icons/>
  </div>
</template>

<script>
import Navbar from "./components/Navbar.vue";
import Home from "./components/Home.vue";
import Icons from "./components/Icons.vue";

export default {
  name: "App",
  components: {
    Navbar,
    Home,
    Icons
  },
};
</script>

<style>
@import url('https://fonts.googleapis.com/css2?family=Poppins&display=swap');
* {
  margin: 0;
  padding: 0;
  box-sizing: border-box;
  font-family: 'Poppins', sans-serif;
}
#app {
  font-family: Avenir, Helvetica, Arial, sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  color: #ffc857;
  height: 100vh;
}
body {
  background: #0f2027; 
  background: -webkit-linear-gradient(
    to right,
    #2c5364,
    #203a43,
    #0f2027
  ); 
  background: linear-gradient(
    to right,
    #2c5364,
    #203a43,
    #0f2027
  );
  height: 100vh;
  overflow: hidden;
}

</style>
