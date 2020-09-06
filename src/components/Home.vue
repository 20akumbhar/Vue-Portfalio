<template>
  <div class="home">
    <img src="@/assets/img.svg" alt />
    <div class="data">
        <h4>Hello, I am</h4>
        <h1>AJINKYA</h1>
        <small><em>Developer</em></small>
        <br>
        <br>
        <button class="btn1" onclick='window.open("https://firebasestorage.googleapis.com/v0/b/ajinkya-kumbhar.appspot.com/o/Resume-2.pdf?alt=media&token=c0f11f00-f8b0-42bf-b580-69bf23503f64");'>
            Download CV
        </button>
        <button class="btn2" v-on:click="contact">
            Contact Me
        </button>
    </div>
  </div>
</template>
<script>
export default {
    methods:{
        contact(){
            this.$router.push('/contact');
        }
    }
}
</script>
<style scoped>
@import url('https://fonts.googleapis.com/css2?family=Rubik:wght@600&display=swap');
.home {
  margin-top: 100px;
  display: flex;
  justify-content: space-evenly;
  flex-wrap: wrap;
  align-items: center;
}
.home img {
  width: 100%;
  max-width: 400px;
  height: auto;
  padding: 20px;
}
.home .data h1{
    color: #ffae0c;
}
.home .data{
    text-align: left;
    margin: 20px 30px;
    font-family: 'Rubik', sans-serif;
}
.home .data button{
    padding: 10px 20px;
    border: 2px solid transparent;
    border-radius: 4px;
    cursor: pointer;
}
.home .data button.btn1{
    background: #ffc857;
    color: #0f2027;
    margin-right: 10px;
}
.home .data button.btn1:hover{
    background: #ffae0c;
}
.home .data button.btn2{
    color: #ffc857;
    background: transparent;
    border: 2px solid #ffc857;
}

.home .data button.btn2:hover{
    color: #0f2027;
    background: #ffc857;
    border: 2px solid #ffc857;
}
em{
    z-index: 9;
    opacity: .6;
}
em::before{
    content: 'Android ';
    animation: textanimation linear 4s infinite;

}
@media only screen and (max-width: 540px) {
    .home{
        margin-top: 40px;
    }
}
@media only screen and (max-width: 450px) {
    .home img{
    width: 70%;
    }
}
@media only screen and (max-width: 350px) {
    .home img{
    width: 100%;
    }
}
@keyframes textanimation{
    0%{
        content: "Android ";
    }
    100%{
        content: "Web ";
    }
}
</style>