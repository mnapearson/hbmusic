<template>
  <div class="contact">
    <Nav />
    <form
      ref="contact"
      class="contact-form"
      @submit.prevent="sendEmail"
      v-if="!successMessage"
    >
      <input type="text" name="user_name" placeholder="name" />

      <input type="email" name="user_email" placeholder="email" />

      <textarea name="message" placeholder="message"></textarea>
      <input type="submit" value="Send" />
    </form>
    <div class="success" v-if="successMessage">
      <p>
        Thank you for your inquiry. <br />You will receive a reply as soon as
        possible.
      </p>
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
.contact {
  position: fixed;
  top: 30%;
  left: 30%;
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
  background: black;
  color: white;
}

.success {
  position: fixed;
  display: flex;
  justify-content: center;
  align-items: center;
  top: 40%;
  left: 40%;
  text-align: center;
}
</style>
