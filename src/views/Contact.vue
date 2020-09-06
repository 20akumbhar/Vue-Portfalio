<template>
  <div class="contact">
    <h2>Contact Me</h2>
    <div class="card">
      <form @submit="send">
        <div class="name">
          <input id="name" type="text" placeholder="Name" v-model="name" required />
        </div>
        <div class="email">
          <input id="email" placeholder="Email Address" type="email" v-model="email" required />
        </div>
        <div class="msg">
          <textarea rows="10" placeholder="Enter Message here.." v-model="msg" required></textarea>
        </div>
        <button>Send</button>
      </form>
      <small>Having Problem , Please send a mail to me at <strong>20akumbhar@gmail.com</strong></small>
    </div>
  </div>
</template>
<script>
const axios = require("axios");
export default {
  data: function () {
    return {
      name: "",
      email: "",
      msg: "",
    };
  },
  methods: {
    async send(e) {
      e.preventDefault();
      let url =
        "https://us-central1-ajinkya-kumbhar.cloudfunctions.net/addMessage?name=" +
        this.name +
        "&email=" +
        this.email +
        "&msg=" +
        this.msg;
      const data  = await axios.get(url);
      //this.data = data;
      console.log(data);
      console.log(this.name);
    },
  },
};
</script>
<style scoped>
.contact {
  margin-top: 80px;
}
.contact h2 {
  text-align: center;
}
.contact .card {
  margin: 20px auto;
  width: 80%;
  background-color: #ffffff1e;
  padding: 20px;
  text-align: center;
}

.contact .card div input,
.contact .card div textarea {
  width: 60%;
  padding: 10px 20px;
  margin: 8px;
  border-radius: 4px;
  border: 1px solid transparent;
}
.contact .card form button {
  padding: 10px 20px;
  background: #ffc857;
  border: 1px solid transparent;
  border-radius: 4px;
  color: #2c5364;
  cursor: pointer;
}
.contact .card form button:hover {
  background: #ffae0c;
}

@media only screen and (max-width: 820px) {
  .contact .card div input,
  .contact .card div textarea {
    width: 80%;
  }
}
@media only screen and (max-width: 520px) {
  .contact .card div input,
  .contact .card div textarea {
    width: 90%;
  }
}
@media only screen and (max-width: 400px) {
  .contact .card {
    width: 95%;
    background-color: #ffffff1e;
    padding: 20px;
    text-align: center;
  }
  .contact .card div input,
  .contact .card div textarea {
    width: 96%;
  }
}
</style>