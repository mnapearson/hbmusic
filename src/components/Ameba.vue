<template>
  <div class="project-details">
    <Nav />
    <div class="project-main">
      <div class="project-left">
        <div class="last-project">
          <router-link class="link" to="/Traumgaben">
            <span
              class="iconify"
              data-inline="false"
              data-icon="dashicons:arrow-left-alt2"
            ></span>
          </router-link>
        </div>
        <div class="project-description">
          <div class="project-title">
            <h3>Ameba</h3>
            <p>Live Hip Hop Jazz Fusion</p>
          </div>
          <div class="project-events">
            <h3>upcoming events</h3>
            <p>06.08.2021 @Casa Pepe, Leipzig</p>
          </div>
        </div>
      </div>
      <div class="project-right">
        <div class="project-right-main">
          <div class="project-image">
            <img src="../images/ameba.jpg" alt="" />
          </div>
          <div class="project-links">
            <!-- <span
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
            ></span>
            <span
              class="iconify"
              data-inline="false"
              data-icon="ei:sc-soundcloud"
            ></span>
            <span
              class="iconify"
              data-inline="false"
              data-icon="bi:youtube"
            ></span> -->
          </div>
        </div>
        <div class="next-project">
          <router-link class="link" to="/BrigadeFutur3">
            <span
              class="iconify"
              data-inline="false"
              data-icon="dashicons:arrow-right-alt2"
            ></span
          ></router-link>
        </div>
      </div>
    </div>
  </div>
</template>

<script>
import Nav from "@/components/Nav.vue";

export default {
  name: "Ameba",
  components: {
    Nav,
  },
};
</script>

<style scoped>
.project-main {
  font-size: 12px;
  line-height: 18px;
  position: fixed;
  display: flex;
  justify-content: center;
  align-items: center;
  top: 50%;
  left: 50%;
  transform: translate(-50%, -50%);
}

.project-left {
  display: flex;
  justify-content: center;
  align-items: center;
  min-width: 60%;
  margin-right: 3rem;
}

.project-right {
  display: flex;
  align-items: center;
}

.project-right-main {
  display: flex;
  flex-direction: column;
  justify-content: center;
  align-items: center;
}
.next-project {
  display: flex;
  align-items: center;
}

.project-right p {
  display: none;
}

.project-image img {
  width: auto;
  height: 250px;
  border: 1px solid;
  margin-bottom: 1rem;
}

.iconify {
  font-size: 20px;
  margin: 0.5rem;
}

.link {
  display: flex;
  justify-content: center;
  align-items: center;
  flex-wrap: nowrap;
  text-decoration: none;
  color: black;
  margin-left: 3rem;
}

.link .iconify {
  margin-right: 3rem;
}

.link :hover {
  color: limegreen;
  text-decoration: bold;
}

a {
  color: black;
}

@media only screen and (max-width: 800px) {
  .project-image img {
    width: auto;
    height: 150px;
    border: 1px solid;
    margin-bottom: 0.3rem;
  }

  .link {
    display: flex;
    justify-content: center;
    align-items: center;
    text-decoration: none;
    color: black;
  }

  .project-right {
    flex-direction: column;
    justify-content: center;
    align-items: center;
  }

  .project-right p {
    display: block;
  }

  .last-project {
    display: none;
  }
}

@media only screen and (max-width: 600px) {
  .project-main {
    flex-direction: column;
    margin-top: 2rem;
    margin-left: 0rem;
    font-size: 10px;
    line-height: 15px;
  }

  .project-left {
    width: 140%;
    margin-right: 0rem;
    margin-bottom: 3rem;
  }

  .project-right {
    margin-bottom: 5rem;
  }

  .project-image img {
    height: 120px;
  }
}
</style>
