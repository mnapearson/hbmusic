<template>
  <div>
    <Nav />
    <div class="events">
      <h3>upcoming events</h3>
      <div class="events-grid">
        <div class="event">
            <p>10.09.21</p>
            <p>19h-21h</p>
            <p>Reso:Kollektiv</p>
            <p>@Gewandhaus</p>
        </div>
        <div class="event">
            <p>29.10.21</p>
            <p>20:00 Uhr</p>
            <router-link class="link" to="/oluma"><p>Oluma</p></router-link>
            <p>@Horns Erben</p>
            <div class="event">
            <p>11.10.2021</p>
            <p>20h-22h</p>
            <p>Ameba</p>
            <p>@Horns Erben</p>
            <div class="event">
            <p>24.05.2022</p>
            <p>19:30h-23h</p>
            <p>Moritz Land Quartet</p>
            <p>@Moritzbastei</p>
            <div class="event">
            <p>03.06.2022</p>
            <p>22:00h - 06:00</p>
            <router-link class="link" to="/oluma"><p>Oluma</p></router-link>
            <p>@Westbahnhof</p>
            <div class="event">
            <p>24.06.2022</p>
            <p>20:30 - 22:00</p>
            <router-link class="link" to="/extraviolette"><p>extraviolette</p></router-link>
            <p>@Substanz, Täubchenweg 67</p>
            <div class="event">
            
            
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

body {
  overflow: hidden;
}

h3 {
  font-size: 12px;
}

p {
  font-size: 12px;
  margin: 0;
}

.link {
  text-decoration: none;
  color: black;
}

.link:hover {
  text-decoration: underline;
}

.events {
  position: fixed;
  top: 50%;
  left: 50%;
  transform: translate(-50%, -50%);
}

.event {
  margin-top: 1rem;
}

@media only screen and (max-width: 800px) {
}

@media only screen and (max-width: 600px) {
}

@media only screen and (max-width: 360px) {
}
</style>
