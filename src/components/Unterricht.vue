<template>
  <div class="project-details">
    <Nav />

    <div class="project-main">
      <div class="project-left">
        <div class="project-description">
          <div class="project-title">
            <h3>saxophon unterricht</h3>
            <p>
              Ich gebe seit 2015 unterricht für Saxophon oder Klarinette. Gerne
              teile ich meine Erfahrungen und Fähigkeiten. Egal ob du Anfänger
              bist oder dich auf ein Musikstudium vorbereitest, kann ich dir
              Wege zeigen wie du alle Aspekte des Musikmachens – das Gehör, die
              Musiktheorie, die Improvisation etc. voran bringst Ich unterrichte
              Privat in meinem Proberaum in Leipzig Großzschocher und an der
              „Neue Musik Leipzig“.
            </p>
            <router-link to="/contact"><p>set up a lesson</p></router-link>
          </div>
          <!-- <div class="project-events">
            <h3>Events</h3>
            <p>date/place</p>
            <p>date/place</p>
          </div> -->
        </div>
      </div>
      <div class="project-right">
        <div class="project-right-main">
          <div class="project-image">
            <img src="../images/proberaum.jpeg" alt="" />
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
      </div>
      <div class="last-project">
        <router-link class="link" to="/BrigadeFutur3">
          <span
            class="iconify"
            data-inline="false"
            data-icon="dashicons:arrow-left-alt2"
          ></span>
        </router-link>
      </div>
    </div>
  </div>
</template>

<script>
import Nav from "@/components/Nav.vue";

export default {
  name: "Unterricht",
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
  flex-direction: column;
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
  .project-main {
    flex-direction: column;
  }

  .project-left {
    margin: 0;
  }

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
    margin: 1rem;
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
    width: 100%;
    margin-right: 0rem;
  }

  .project-right {
    margin-top: 3rem;
    margin-bottom: 5rem;
  }

  .project-image img {
    height: 120px;
  }
}
</style>
