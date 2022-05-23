<template>
  <div class="project-details">
    <Nav />
    <div class="project-main">
      <div class="project-left">
        <div class="project-description">
          <h3>extraviolette</h3>
          <p>
            Die Floral Geräucherte extra heiße Band, die selbst den Papst zum
            tanzen kriegt ist ready . Extraviolette steht für Disco, Liebe,
            Vielfalt, Loslassen, Befreiung und die Nacht durch-tanzen.
            Extraviolette ist die Farbe der Emanzipation – Emanzipation aller
            Geschlechter und Gedanken, die Farbe der Verwandlung, der
            Inspiration und der Individualität. Sie will euch auf eine Auszeit
            für eure Sorgen mitnehmen und macht einen „extra“ Workout für euer
            inneres Licht und eure Füße. Inspiriert von dem Geist und der
            Energie der Discoera der 1970er Jahre, bringen sie eine mitreißende
            Show auf die Bühne, in der man sich gerne verliert.
          </p>
          <p>
            Die 9 Musiker*innen aus Leipzig sind im dritten Jahr ihres Bestehens
            zu einer schlagfertigen Truppe zusammengewachsen, mit dem Ziel ihren
            Sound und ihre Liebe zu Disco, Funk und Soul auf die Tanzflächen
            dieser Welt zu bringen. Die Party ist da wo sie sind! Stay tuned!
          </p>
        </div>
        <div class="project-events">
          <h3>upcoming events</h3>
          <p>24.06.22
             20:30 
             @Substanz, Täubchenweg 67 
             Leipzig</p>
        </div>
      </div>
      <div class="project-right">
        <div class="project-right-main">
          <div class="project-image">
            <a
              target="_blank"
              rel="noopener noreferrer"
              href="https://extraviolette.de/"
            >
              <img src="../images/extraviolette.jpg" alt=""
            /></a>
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
            ></span>-->
            <a
              target="_blank"
              rel="noopener noreferrer"
              href="https://www.facebook.com/Extraviolette/"
            ></a>
            <span
              class="iconify"
              data-inline="false"
              data-icon="bi:facebook"
            ></span>
            <a
              target="_blank"
              rel="noopener noreferrer"
              href="https://www.instagram.com/extra.violette/"
            ></a>
            <span
              class="iconify"
              data-inline="false"
              data-icon="bi:instagram"
            ></span>
            <a
              target="_blank"
              rel="noopener noreferrer"
              href="https://www.youtube.com/watch?v=-okFMwPcBYA"
              ><span
                class="iconify"
                data-inline="false"
                data-icon="bi:youtube"
              ></span
            ></a>
          </div>
        </div>
        <div class="next-project">
          <router-link class="link" to="/Oluma">
           
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
  name: "Extraviolette",
  components: {
    Nav,
  },
};
</script>

<style scoped>
.project-main {
  position: fixed;
  display: flex;
  justify-content: center;
  align-items: center;
  top: 50%;
  left: 50%;
  transform: translate(-50%, -50%);
  font-size: 12px;
  line-height: 18px;
}

.project-left {
  min-width: 60%;
  margin-right: 4rem;
}

.project-right {
  display: flex;
  align-items: center;
}

.project-right p {
  display: none;
}

.next-project {
  display: flex;
  align-items: center;
}

.project-right-main {
  display: flex;
  flex-direction: column;
  justify-content: center;
  align-items: center;
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
  margin-left: 2rem;
}

.link .iconify {
  margin: 0;
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
  }

  .project-right p {
    display: block;
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
