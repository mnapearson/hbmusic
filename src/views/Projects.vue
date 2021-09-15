<template>
  <div class="projects">
    <Nav />
    <div class="projects-grid">
      <div class="project one">
        <router-link class="link" to="/Extraviolette">
          <div class="container">
            <div class="centered">extraviolette</div>
            <img src="../images/extraviolette.jpg" alt="" />
          </div>
        </router-link>
      </div>
      <div class="project two">
        <router-link class="link" to="/Oluma">
          <div class="container">
            <div class="centered">oluma</div>
            <img src="../images/Oluma.jpg" alt="" /></div
        ></router-link>
      </div>
      <div class="project three">
        <router-link class="link" to="/Traumgaben">
          <div class="container">
            <div class="centered">traumgaben</div>
            <img src="../images/traumgaben.png" alt="" /></div
        ></router-link>
      </div>
      <div class="project four">
        <router-link class="link" to="/Ameba">
          <div class="container">
            <div class="centered">ameba</div>
            <img src="../images/ameba.jpg" alt="" /></div
        ></router-link>
      </div>
      <div class="project five">
        <router-link class="link" to="/BrigadeFutur3">
          <div class="container">
            <div class="centered">brigade futur 3</div>
            <img src="../images/brigadefutur3.png" alt="" /></div
        ></router-link>
      </div>
      <div class="project six">
        <router-link class="link" to="/Unterricht">
          <div class="container">
            <div class="centered">saxophon unterricht</div>
            <img src="../images/teacher.jpg" alt="" /></div
        ></router-link>
      </div>
    </div>
    <router-link class="events-link" to="/events">Upcoming events</router-link>
  </div>
</template>

<script>
import Nav from "@/components/Nav.vue";

export default {
  name: "Projects",
  components: {
    Nav,
  },
};
</script>

<style scoped>
.projects-grid {
  position: fixed;
  display: inline-grid;
  top: 50%;
  left: 50%;
  transform: translate(-50%, -50%);
}

.project {
  width: 200px;
  height: 200px;
  margin: 1rem;
  font-size: 12px;
  border: 1px solid black;
}

.project img {
  width: 200px;
  height: 200px;
}

.container {
  position: relative;
  text-align: center;
  color: white;
}

.centered {
  position: absolute;
  top: 50%;
  left: 50%;
  transform: translate(-50%, -50%);
  background-color: black;
  padding: 0.5rem 1rem;
}

.link {
  text-decoration: none;
  color: black;
}

.events-link {
  position: fixed;
  top: 90%;
  left: 50%;
  transform: translate(-50%, -50%);
  text-decoration: underline;
  text-transform: lowercase;
  color: black;
  font-size: 12px;
}

.events-link:hover {
  color: green;
  font-weight: bold;
}

.link :hover {
  color: limegreen;
  text-decoration: bold;
}

.one {
  grid-column: 1;
  grid-row: 1;
}

.two {
  grid-column: 2;
  grid-row: 1;
}

.three {
  grid-column: 3;
  grid-row: 1;
}

@media only screen and (max-width: 800px) {
  .one {
    grid-column: 1;
    grid-row: 1;
  }

  .two {
    grid-column: 2;
    grid-row: 1;
  }

  .three {
    grid-column: 1;
    grid-row: 2;
  }

  .four {
    grid-column: 2;
    grid-row: 2;
  }
}

@media only screen and (max-width: 600px) {
  .project {
    width: 120px;
    height: 120px;
    margin: 0.4rem;
    font-size: 10px;
    border: 1px solid black;
  }

  .project img {
    width: 120px;
    height: 120px;
  }
}

@media only screen and (max-width: 360px) {
}
</style>
