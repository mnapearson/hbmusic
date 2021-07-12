<template>
  <div class="contact">
    <Nav />
    <div class="contact-main">
      <div class="contact-image">
        <img src="../images/henrikcontact.png" alt="" />
      </div>
      <div class="contact-form">
        <form
          ref="contact"
          class="contact-form"
          @submit.prevent="sendEmail"
          v-if="!successMessage"
        >
          <p>get in touch</p>
          <input type="text" name="user_name" placeholder="name" />

          <input type="email" name="user_email" placeholder="email" />

          <textarea name="message" placeholder="message"></textarea>
          <input type="submit" value="Send" />
        </form>
        <p v-if="successMessage">
          Thank you for your message. <br />You will receive a reply as soon as
          possible.
        </p>
      </div>
    </div>
  </div>
</template>

<script>
import Nav from "@/components/Nav.vue";
import emailjs from "emailjs-com";

export default {
  name: "Contact",
  components: {
    Nav,
  },
  data() {
    return {
      name: "",
      email: "",
      message: "",
      successMessage: false,
    };
  },
  methods: {
    sendEmail(e) {
      try {
        emailjs.sendForm(
          "service_9kxr7d6",
          "template_yffeype",
          e.target,
          "user_o6tM95YAVRykwYE7z90AI",
          {
            name: this.name,
            email: this.email,
            message: this.message,
          }
        );
      } catch (error) {
        console.log({ error });
      }
      // Reset form field
      this.name = "";
      this.email = "";
      this.message = "";
      this.successMessage = true;
    },
  },
};
</script>

<style scoped>
.contact-main {
  position: fixed;
  display: flex;
  top: 50%;
  left: 50%;
  transform: translate(-50%, -50%);
  justify-content: center;
  align-items: center;
}

.contact-image img {
  height: 400px;
}

.contact-image {
  margin-right: 3rem;
}

.contact-form {
  text-align: center;
  font-size: 12px;
  line-height: 22px;
  min-width: 70%;
}

label {
  float: left;
}

input[type="text"],
[type="email"],
textarea {
  width: 100%;
  padding: 12px;
  box-sizing: border-box;
  margin-top: 6px;
  margin-bottom: 16px;
}

input[type="submit"] {
  padding: 12px 20px;
  border: none;
  border-radius: 4px;
  cursor: pointer;
}

input[type="submit"]:hover {
  background: black;
  color: white;
}

.success {
  position: fixed;
  display: flex;
  justify-content: center;
  align-items: center;
  text-align: center;
}
</style>
