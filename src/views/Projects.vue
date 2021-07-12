<template>
  <div class="projects">
    <Nav />
    <div class="projects-grid">
      <div class="project one">
        <router-link class="link" to="/project-one"
          ><p>project one</p></router-link
        >
      </div>
      <div class="project two">
        <router-link class="link" to="/project-two"
          ><p>project two</p></router-link
        >
      </div>
      <div class="project three">
        <router-link class="link" to="/project-three"
          ><p>project three</p></router-link
        >
      </div>
      <div class="project four">
        <router-link class="link" to="/project-four"
          ><p>project four</p></router-link
        >
      </div>
      <div class="project five">
        <router-link class="link" to="/project-five"
          ><p>project five</p></router-link
        >
      </div>
      <div class="project six">
        <router-link class="link" to="/project-six"
          ><p>project six</p></router-link
        >
      </div>
    </div>
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
  display: flex;
  justify-content: center;
  align-items: center;
  text-align: center;
  width: 200px;
  height: 200px;
  border: 1px solid black;
  margin: 1rem;
  font-size: 12px;
  line-height: 22px;
}

.link {
  text-decoration: none;
  color: black;
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
</style>
