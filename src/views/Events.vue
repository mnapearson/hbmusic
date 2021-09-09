<template>
  <div>
    <Nav />
    <div class="events">
      <h3>upcoming events</h3>
      <div class="events-grid">
        <div class="date">
          <p>09.09.21</p>
          <p>10.09.21</p>
        </div>
        <div class="time">
          <p>12h - 17h</p>
          <p>19h-21h</p>
        </div>
        <div class="project">
          <router-link class="link" to="/project-three"
            ><p>Traumgaben</p></router-link
          >
          <p>Reso:Kollektiv</p>
        </div>
        <div class="location">
          <p>@Pittlerwerke</p>
          <p>@Gewandhaus</p>
        </div>
      </div>
    </div>
  </div>
</template>

<script>
import Nav from "@/components/Nav.vue";

export default {
  name: "Events",
  components: {
    Nav,
  },
};
</script>

<style scoped>
h3 {
  font-size: 12px;
}

p {
  font-size: 12px;
}

.events {
  position: fixed;
  top: 50%;
  left: 50%;
  transform: translate(-50%, -50%);
}

.events-grid {
  display: grid;
  grid-auto-columns: 1fr 1fr 1fr 1fr;
}

.events-grid p {
  margin: 1rem;
}

.link {
  text-decoration: none;
  color: black;
}

.date {
  grid-column: 1;
}

.time {
  grid-column: 2;
}

.project {
  grid-column: 3;
}

.location {
  grid-column: 4;
}
</style>
