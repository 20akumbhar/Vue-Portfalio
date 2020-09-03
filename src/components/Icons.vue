<template>
  <div class="icons">
    <div class="icon">
      <div class="name">Github</div>
      <img src="@/assets/github.svg" alt />
    </div>
    <div class="icon">
      <div class="name">Instagram</div>
      <img src="@/assets/instagram.svg" alt />
    </div>
    <div class="icon">
      <div class="name">LinkedIn</div>
      <img src="@/assets/linkedin.svg" alt />
    </div>
    <div class="icon">
      <div class="name">Whatsapp</div>
      <img src="@/assets/whatsapp.svg" alt />
    </div>
    <div class="icon">
      <div class="name">Blogger</div>
      <img src="@/assets/blogger.svg" alt />
    </div>
  </div>
</template>
<style scoped>
.icons {
  position: absolute;
  top: 50%;
  left: 0;
  display: flex;
  flex-direction: column;
  transform: translateY(-50%);
}
.icons .icon {
  cursor: pointer;
  transform: translateX(-100px);
  display: flex;
  padding: 10px;
  background-color: #ffc857;
  transition: ease-in-out 0.4s;
}
.icons .icon .name {
  width: 100px;
  color: #2c5364;
}
.icons .icon img {
  width: 26px;
  height: 26px;
}
.icons .icon:hover {
  transform: translateX(0px);
  transition: ease-in-out 0.4s;
}
@media only screen and (max-width: 450px) {
  .icons {
    bottom: 0;
    top: auto;
    left: 50%;
    margin-top: auto;
    transform: translateY(0%);
    flex-direction: row;
    transform: translateX(-50%);
  }

  .icons .icon{
      transform: translateX(0px);
  }
  .icons .icon .name {
    display: none;

  }
  .icons .icon:hover {
    transform: translateY(-2px);
    transition: ease-in-out 0.4s;
  }
}
</style>