<template>
  <div class="contact">
    <Nav />
    <form ref="contact" class="contact-form" @submit.prevent="sendEmail">
      <label>Name</label>
      <input type="text" name="user_name" />
      <label>Email</label>
      <input type="email" name="user_email" />
      <label>Message</label>
      <textarea name="message"></textarea>
      <input type="submit" value="Send" />
    </form>
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
  methods: {
    sendEmail: (e) => {
      emailjs
        .sendForm(
          "service_9kxr7d6",
          "template_yffeype",
          e.target,
          "user_o6tM95YAVRykwYE7z90AI"
        )
        .then(
          (result) => {
            console.log("SUCCESS!", result.status, result.text);
          },
          (error) => {
            console.log("FAILED...", error);
          }
        );
      this.$refs.contact.resetFields();
    },
  },
};
</script>

<style scoped>
.contact {
  position: fixed;
  top: 30%;
  left: 20%;
}

.container {
  display: block;
  margin: auto;
  text-align: center;
  border-radius: 5px;
  padding: 20px;
  width: 50%;
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
  resize: vertical;
}

input[type="submit"] {
  padding: 12px 20px;
  border: none;
  border-radius: 4px;
  cursor: pointer;
}

input[type="submit"]:hover {
}
</style>
