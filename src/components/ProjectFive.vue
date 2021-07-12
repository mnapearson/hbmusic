<template>
  <div class="project-details">
    <Nav />
    <div class="project-main">
      <div class="project-left">
        <div class="last-project">
          <router-link class="link" to="/project-four">
            <span
              class="iconify"
              data-inline="false"
              data-icon="dashicons:arrow-left-alt2"
            ></span>
          </router-link>
        </div>
        <div class="project-description">
          <div class="project-title">
            <h3>Project Five</h3>
            <p>
              Lorem ipsum, dolor sit amet consectetur adipisicing elit. Repellat
              laborum quisquam, natus quia sequi, doloremque quo illo omnis,
              veritatis consectetur iste? Repudiandae perferendis odit, unde,
              mollitia facere voluptas error sit voluptatibus, aspernatur
              debitis alias quos quo suscipit laborum reiciendis voluptatem.
            </p>
          </div>
          <div class="project-events">
            <h3>Events</h3>
            <p>date/place</p>
            <p>date/place</p>
          </div>
        </div>
      </div>
      <div class="project-right">
        <div class="project-image"></div>
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
          ></span>
        </div>
      </div>
      <div class="next-project">
        <router-link class="link" to="/project-six">
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
  name: "ProjectFive",
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
}

.project-left {
  display: flex;
  justify-content: center;
  align-items: center;
  min-width: 70%;
  margin-right: 3rem;
}

.project-right {
  display: flex;
  flex-direction: column;
  justify-content: center;
  align-items: center;
}

.project-image {
  width: 200px;
  height: 200px;
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

.link p {
  margin: 0;
  line-height: 10px;
}

.link .iconify {
  margin-right: 3rem;
}

.link :hover {
  color: limegreen;
  text-decoration: bold;
}
</style>
