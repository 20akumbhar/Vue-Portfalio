<template>
  <div id="app">
    <Navbar/>
    
    <router-view/>
    <Icons/>
  </div>
</template>

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

<script>
import Navbar from './components/Navbar';
import Icons from './components/Icons';

export default {
  name: "App",
  components: {
    Navbar,
    Icons
  },
}
</script>