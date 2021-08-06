<template>
  <div class="project-details">
    <Nav />
    <div class="project-main">
      <div class="project-left">
        <div class="last-project">
          <router-link class="link" to="/project-one">
            <span
              class="iconify"
              data-inline="false"
              data-icon="dashicons:arrow-left-alt2"
            ></span>
          </router-link>
        </div>
        <div class="project-description">
          <div class="project-title">
            <h3>oluma</h3>
            <p>
              OLUMA besteht aus neun jungen Musiker*innen, die ihre Leidenschaft
              für Musik teilen, die vom Afrobeat der späten 60er und der 70er
              Jahre inspiriert wurde.Gegründet vom Bassisten Gregor Nicolai,
              Drummer André van der Heide und Saxophonist Roman Polatzky, hat
              sich der Rest der Band während des Musikstudiums gefunden.Ihr
              Sound ist vor allem von West-Afrikanischer und Brasilianischer
              Musik, sowie Funk und Jazz beeinflusst.
            </p>
            <p>
              Erstmals veröffentlicht hat die Band ihre Musik in einer
              Live-Session aus dem NEUES SCHAUSPIEL Leipzig. Die drei dabei
              entstanden Videos gibt es auf ihrem Youtube-Kanal - Schaut gerne
              vorbei und lasst ein Abo da.
            </p>
          </div>
          <div class="project-events">
            <h3>upcoming shows</h3>
            <p>14.08.2021 @Roots & Sprouts Festival- Leipzig</p>
            <p>
              03.09.2021 @Musikfestival Künstlerhaus- Colditz Colditz/Leipzig
            </p>
            <p>29.10.2021 @Horns Erben- Arndtstraße 33, 04275 Leipzig</p>
          </div>
        </div>
      </div>
      <div class="project-right">
        <div class="project-right-main">
          <div class="project-image">
            <img src="../images/Oluma.jpg" alt="" />
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
            ></span>
            <span
              class="iconify"
              data-inline="false"
              data-icon="ei:sc-soundcloud"
            ></span>
            <a href="https://www.youtube.com/channel/UCiuIOZLXOO0DTyKJrccaM1Q"
              ><span
                class="iconify"
                data-inline="false"
                data-icon="bi:youtube"
              ></span
            ></a>
          </div>
        </div>
        <div class="next-project">
          <router-link class="link" to="/project-three">
            <p>next project</p>
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
  name: "ProjectTwo",
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
    width: 140%;
    margin-right: 0rem;
  }

  .project-right {
    margin-bottom: 5rem;
  }

  .project-image img {
    height: 120px;
  }
}
</style>
