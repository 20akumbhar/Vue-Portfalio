<template>
  <div class="about">
    <br>
    <br>
    <h2>About Me</h2>
    <div class="data">
      <div class="info">
        Hello, <br>
          My name is 
          <br>
          <strong> Ajinkya Santosh Kumbhar</strong>.
          <br>
          To know all about me, <br>
          <button onclick='window.open("https://firebasestorage.googleapis.com/v0/b/ajinkya-kumbhar.appspot.com/o/Resume-2.pdf?alt=media&token=c0f11f00-f8b0-42bf-b580-69bf23503f64");'>Get CV</button>
      </div>
      <div class="img">
        <img src="@/assets/code.svg" alt="">
      </div>
    </div>
  </div>
</template>
<style scoped>
.about h2{
  margin-top: 20px;
  text-align: center;
}
.about .data {
  margin-top: 20px;
  display: flex;
  justify-content: space-evenly;
  flex-wrap: wrap-reverse;
  align-items: center;
}
.about .data .info{
  margin: 60px;
}
.about .data .info button{
padding: 10px 20px;
margin-top: 20px;
font-weight: bold;
background: #ffc857;
border: 2px solid transparent;
border-radius: 4px;
cursor: pointer;
color: #2c5364;
}
.about .data .info button:hover{
    background: #ffae0c;
}
.about .data .img{
  padding: 40px;
}
.about .data .img img{
  width: 100%;
  height: auto;
  max-width: 600px;
}
</style>