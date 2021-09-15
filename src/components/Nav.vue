<template>
  <div class="nav-main">
    <nav>
      <cookie-law theme="base"></cookie-law>
      <div class="top">
        <router-link class="link" to="/">Henrik Baumgarten</router-link>
      </div>
      <div class="left">
        <router-link class="link one" to="/about">About</router-link>
        <!-- <router-link class="link two" to="/blog">Blog</router-link> -->
      </div>
      <div class="bottom">
        <router-link class="link" to="/contact">Contact</router-link>
      </div>
      <div class="right">
        <router-link class="link one" to="/projects">Projects</router-link>
      </div>
    </nav>
  </div>
</template>

<script>
import CookieLaw from "vue-cookie-law";

export default {
  components: { CookieLaw },
  name: "Nav",
};
</script>

<style scoped>
.link {
  text-decoration: none;
  text-transform: uppercase;
  color: black;
  font-size: 12px;
}
.top {
  position: fixed;
  display: flex;
  top: 0;
  left: 50%;
  margin-top: 2rem;
  transform: translate(-50%, -50%);
}
.top .link:hover,
.top .router-link-exact-active {
  color: purple;
  font-weight: bold;
}

.left {
  position: fixed;
  display: flex;
  left: 0;
  top: 50%;

  transform: rotate(-90deg);
}

.left .link {
  margin-left: 1rem;
}

.right .link {
  margin-right: 1rem;
}

.left .link:hover,
.left .router-link-active {
  color: orange;
  font-weight: bold;
}

.left .two:hover {
  color: darkgray;
}

.bottom {
  position: fixed;
  display: flex;
  bottom: 0;
  left: 50%;
  margin-bottom: 1rem;
  transform: translate(-50%, -50%);
}
.bottom .link:hover,
.bottom .router-link-active {
  color: red;
  font-weight: bold;
}

.right {
  position: fixed;
  display: flex;
  right: 0;
  top: 50%;
  transform: rotate(90deg);
}

.right:hover {
  color: blue;
  font-weight: bold;
}

.right .router-link-exact-active {
  color: blue;
  font-weight: bold;
}

@media only screen and (max-width: 800px) {
  .audio {
    right: 10%;
  }
}

@media only screen and (max-width: 600px) {
  .audio img {
    width: 20px;
    height: 20px;
  }

  .audio {
    right: 10%;
  }

  .top {
    top: 25%;
    margin-top: 0rem;
  }

  .left {
    left: 2%;
    margin-left: 0;
  }

  .right {
    right: 2%;
    margin-right: 0;
  }

  .bottom {
    bottom: 25%;
    margin-bottom: 0;
  }
}

@media only screen and (max-width: 450px) {
  img {
    height: 300px;
  }

  .top {
    top: 3%;
    margin-top: 0rem;
  }

  .left {
    left: 0;
  }

  .right {
    right: 0;
  }

  .bottom {
    bottom: 2%;
    margin-bottom: 0;
  }
}
</style>
