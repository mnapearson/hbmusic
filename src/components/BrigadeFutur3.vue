<template>
  <div class="project-details">
    <Nav />
    <div class="project-main">
      <div class="project-left">
        <div class="last-project">
          <router-link class="link" to="/Ameba">
            <span
              class="iconify"
              data-inline="false"
              data-icon="dashicons:arrow-left-alt2"
            ></span>
          </router-link>
        </div>
        <div class="project-description">
          <div class="project-title">
            <h3>Brigade Futur 3</h3>
            <p>
              Die Antikapitalistische Kampfband.! Eine Kooperation Aus Berlin
              und Leipzig. Schaut mal rein und kauft weniger!
            </p>
          </div>
          <div class="project-events">
            <h3>upcoming events</h3>
            <p>tbd</p>
          </div>
        </div>
      </div>
      <div class="project-right">
        <div class="project-right-main">
          <div class="project-image">
            <a
              target="_blank"
              rel="noopener noreferrer"
              href="https://www.brigadefutur3.org/"
            >
              <img src="../images/brigadefutur3.png" alt="" />
            </a>
          </div>
          <div class="project-links">
            <a href="https://open.spotify.com/album/0ePxWyTIpepcISBETJUizq">
              <span
                class="iconify"
                data-inline="false"
                data-icon="akar-icons:spotify-fill"
              ></span></a
            ><a
              href="https://music.apple.com/de/album/alles-wird-gut-gegangen-sein-werden/1306726253?app=music"
            >
              <span
                class="iconify"
                data-inline="false"
                data-icon="cib:apple-music"
              ></span></a
            ><a
              href="https://whyplayjazz.bandcamp.com/album/alles-wird-gut-gegangen-sein-werden"
            >
              <span
                class="iconify"
                data-inline="false"
                data-icon="simple-icons:bandcamp"
              ></span></a
            ><a
              href="https://soundcloud.com/whyplayjazz/brigade-futur-iii-alles-wird-gut-gegangen-sein-werden-album-teaser"
            >
              <span
                class="iconify"
                data-inline="false"
                data-icon="ei:sc-soundcloud"
              ></span></a
            ><a href="https://www.youtube.com/watch?v=sboblPq5Mfo&t=2s">
              <span
                class="iconify"
                data-inline="false"
                data-icon="bi:youtube"
              ></span
            ></a>
          </div>
        </div>
      </div>
      <div class="next-project">
        <router-link class="link" to="/Unterricht">
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
  name: "BrigadeFutur3",
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

  .next-project {
    margin-bottom: 3rem;
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
