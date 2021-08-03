<template>
  <div class="project-details">
    <Nav />
    <div class="project-main">
      <div class="project-left">
        <div class="last-project">
          <router-link class="link" to="/project-two">
            <span
              class="iconify"
              data-inline="false"
              data-icon="dashicons:arrow-left-alt2"
            ></span>
          </router-link>
        </div>
        <div class="project-description">
          <div class="project-title">
            <h3>Traumgaben</h3>
            <p>My own Jazz.</p>
          </div>
          <div class="project-events">
            <h3>upcoming shows</h3>
            <p>tbd</p>
          </div>
        </div>
      </div>
      <div class="project-right">
        <div class="project-image">
          <img src="../images/traumgaben.png" alt="" />
        </div>
        <div class="project-links">
          <span
            class="iconify"
            data-inline="false"
            data-icon="akar-icons:spotify-fill"
          ></span>
          <span
            class="iconify"
            data-inline="false"
            data-icon="cib:apple-music"
          ></span>
          <span
            class="iconify"
            data-inline="false"
            data-icon="simple-icons:bandcamp"
          ></span
          ><a
            href="https://soundcloud.com/traumgaben?fbclid=IwAR3UTIaZ5rpU9cto199dx9xAWlyddN5iBKidQKVlCWNPo57g3lFPNF2Uqp4"
          >
            <span
              class="iconify"
              data-inline="false"
              data-icon="ei:sc-soundcloud"
            ></span
          ></a>
          <span
            class="iconify"
            data-inline="false"
            data-icon="bi:youtube"
          ></span>
        </div>
      </div>
      <div class="next-project">
        <router-link class="link" to="/project-four">
          <span
            class="iconify"
            data-inline="false"
            data-icon="dashicons:arrow-right-alt2"
          ></span
        ></router-link>
      </div>
    </div>
  </div>
</template>

<script>
import Nav from "@/components/Nav.vue";

export default {
  name: "ProjectSix",
  components: {
    Nav,
  },
};
</script>

<style scoped>
* {
  font-size: 12px;
  line-height: 18px;
}

.project-main {
  position: fixed;
  display: flex;
  justify-content: center;
  align-items: center;
  top: 50%;
  left: 50%;
  transform: translate(-50%, -50%);
  margin-right: 3rem;
}

.project-left {
  display: flex;
  justify-content: center;
  align-items: center;
  min-width: 70%;
  margin-right: 5rem;
}

.project-right {
  display: flex;
  flex-direction: column;
  justify-content: center;
  align-items: center;
}

.project-image img {
  width: auto;
  height: 300px;
  border: 1px solid;
  margin-bottom: 1rem;
}

.iconify {
  font-size: 20px;
  margin: 0.5rem;
}

a {
  color: black;
  text-decoration: none;
}

.link {
  display: flex;
  justify-content: center;
  align-items: center;
  flex-wrap: nowrap;
  text-decoration: none;
  color: black;
  margin-right: 3rem;
}

.link p {
  margin: 0;
  line-height: 10px;
}

.link .iconify {
  margin-right: 0.2rem;
}

.link :hover {
  color: limegreen;
  text-decoration: bold;
}
</style>
