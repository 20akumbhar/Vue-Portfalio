<template>
  <div class="services">
    <h2>Services</h2>
   
      <slider animation="normal" indicators="center" :control-btn="btn" :touch="touch" >
        <slider-item>
            <img class="slider-img" src="@/assets/android.svg" alt="">
            <br>
            <br>
            <h2>Android Development</h2>
        </slider-item>
        <slider-item>
            <img class="slider-img" src="@/assets/web.svg" alt="">
           <br>
           <br>
            <h2>Web Development</h2>
        </slider-item>
        <slider-item>
            <img class="slider-img" src="@/assets/backend.svg" alt="">
           <br>
           <br>
            <h2>Backend Development</h2>
        </slider-item>
      </slider>
    
  </div>
</template>
<script>
import { Slider, SliderItem } from "vue-easy-slider";
export default {
  components: {
    Slider,
    SliderItem,
  },
  data: function(){
      return{
          btn: false,
          touch: true
      }
  }
};
</script>
<style scoped>
.services {
  margin: 80px 60px;
}
.services h2 {
  text-align: center;
}

.slider{
    text-align: center;
    margin-top: 40px;
    background-color: transparent;
    /* background-color: rgba(255, 255, 255, 0.055); */
}
.slider-btn{
    background: none !important;
}

.slider .slider-items .slider-item{
    padding: 20px;

}
.slider-img{
    width: 200px;
    height: auto;
}
@media only screen and (max-width: 450px) {
    .services {
        margin: 60px 10px;
    }
}
</style>