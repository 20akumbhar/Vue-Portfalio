<template>
  <nav>
    <div class="brand">Ajinkya</div>
    <div class="menu" v-on:click="toggle">
      <svg class="fill-current h-3 w-3" viewBox="0 0 20 20" xmlns="http://www.w3.org/2000/svg">
        <title>Menu</title>
        <path d="M0 3h20v2H0V3zm0 6h20v2H0V9zm0 6h20v2H0v-2z" />
      </svg>
    </div>
    <div class="opt" v-bind:class="{ton : active}">
      <ul>
        <li class="active">Home</li>
        <li>About</li>
        <li>Services</li>
        <li>Contact</li>
      </ul>
    </div>
  </nav>
</template>


<script>
export default {
  data: function () {
    return { active: false };
  },
  methods: {
    toggle() {
      this.active = !this.active;
    },
  },
};
</script>


<style scoped>
nav {
  position: fixed;
  top: 0;
  height: 60px;
  width: 100%;
  padding: 10px 20px;
  background-color: transparent;
  color: #ffc857;
  /* border-bottom: 1px solid #ffc857; */
}
nav .brand {
  padding: 10px;
  display: inline-block;
  font-size: 20px;
}
nav .menu {
  display: none;
  height: 18px;
  width: 18px;
  float: right;
  margin: 10px;
}
nav .menu svg {
  fill: #ffc857;
}
nav .opt {
  z-index: 99999;
  float: right;
}
nav .opt ul {
  list-style: none;
}
nav .opt ul li {
  float: right;
  padding: 10px 20px;
}
nav .opt ul li.active,nav .opt ul li:hover{
  border-bottom: 1px solid #ffc857;
}
@media only screen and (max-width: 600px) {
  nav .menu {
    display: block;
  }
  nav .opt {
    height: 100vh;
    position: absolute;
    top: 60px;
    left: 0;
    color: #ff632a;
    background: #0f2027;
    background: -webkit-linear-gradient(to right, #2c5364, #203a43, #0f2027);
    background: linear-gradient(to right, #2c5364, #203a43, #0f2027);
    max-width: 0%;
    overflow: hidden;
    margin: 0;
  }
  nav .opt.ton {
    min-width: 100% !important;
  }
  nav .opt ul {
    z-index: 99;
    display: block;
    float: unset;
    margin-top: 60px;
    color: #ffc857;
  }
  nav .opt ul li {
    float: unset;
    display: block;
    padding: 30px;
    text-align: center;
  }
}
</style>