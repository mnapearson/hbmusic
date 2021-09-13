<template>
  <div>
    <div class="contact">
      <Nav />
      <div class="contact-main">
        <div class="contact-image">
          <div class="image">
            <img
              class="mobile-image"
              src="../images/henrikcontact.png"
              alt=""
            />
            <router-link
              class="link"
              to="/privacy"
              target="_blank"
              rel="noopener noreferrer"
            >
              <p>privacy policy</p></router-link
            >
          </div>
        </div>

        <div class="contact-form">
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
          <p v-if="successMessage">
            Thank you for your message. <br />You will receive a reply as soon
            as possible.
          </p>
        </div>
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
  min-width: 70%;
}

.link {
  font-size: 10px;
  text-transform: lowercase;
  text-decoration: none;
  color: black;
}

.link:hover {
  text-decoration: underline;
}

label {
  float: left;
}

input[type="text"],
[type="email"],
textarea {
  width: 100%;
  padding: 10px;
  margin-top: 6px;
  margin-bottom: 16px;
  border: 1px solid black;
  border-radius: 4px;
}

textarea {
  height: 150px;
}

input[type="submit"] {
  padding: 10px 20px;
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

@media only screen and (max-width: 800px) {
  .contact-main {
    flex-direction: column;
  }
  .contact-image {
    margin: 0;
  }

  .contact-image img {
    height: 300px;
  }

  .contact-form {
    margin-top: 1rem;
  }
}

@media only screen and (max-width: 600px) {
  .mobile-image {
    margin-top: 2rem;
  }

  .contact-image img {
    height: 200px;
  }

  .contact-form {
    margin-bottom: 2rem;
  }
}

@media only screen and (max-width: 360px) {
  .mobile-image {
    display: none;
  }
}
</style>
