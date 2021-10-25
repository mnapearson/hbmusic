<template>
  <div class="about">
    <Nav />
    <div class="about-content">
      <div class="about-text">
        <p>
          Henrik Baumgarten ist ein professioneller Saxophonist, aus Leipzig.
          Angefangen im Landesjugendjazzorchester Brandenburg, unter Jiggs
          Whigham., 2006 steht er seit 2007 mit den verschiedensten Formationen
          auf der Bühne. Es folgten während seines Saxophonstudiums 2010 - 2015
          die projekte
          <a
            target="_blank"
            rel="noopener noreferrer"
            href="https://www.youtube.com/watch?v=iP3sJYubXPk"
          >
            T.O.Y.</a
          >, Engagements im Leipziger Central Theater und regelmäßige Auftritte
          in der leipziger Jazzszene.
        </p>
        <p>
          In dieser Zeit erlernte er auch autodidaktisch Klarinette und
          Querflöte. 2015-2020 war er Mitglied in der in Leipzig ansässigen
          BigBand „Spielvereinigung Sued“ und deren Kooperation „Brigade Futur
          III“ Musikalisch fühlt er sich vor allem seinen Instrumenten
          verpflichtet und versucht in seiner Musik die klanglichen
          Möglichkeiten des Saxophons und der Klarinette auszureizen.
          Instrumentaler Freigeist mit Mut zum Kitsch.
        </p>
      </div>
      <div class="about-carousel">
        <img src="../images/henrikslide1.png" alt="" />
        <img class="mobile-hidden" src="../images/henrikslide2.png" alt="" />
      </div>
    </div>
  </div>
</template>

<script>
// @ is an alias to /src
import Nav from "@/components/Nav.vue";

export default {
  name: "About",
  components: {
    Nav,
  },
};
</script>

<style scoped>
body {
  overflow: hidden;
}

.about-content {
  display: flex;
  position: fixed;
  top: 50%;
  left: 50%;
  transform: translate(-50%, -50%);
  justify-content: center;
  align-items: center;
}

.about-text {
  font-size: 12px;
  line-height: 22px;
  min-width: 50%;
  margin-right: 3rem;
}

.about-carousel {
  display: flex;
  flex-direction: column;
  justify-content: center;
  align-items: center;
}

img {
  width: 350px;
  margin-bottom: 1rem;
}

@media only screen and (max-width: 800px) {
  .about-content {
    flex-direction: column;
  }

  .about-carousel {
    display: flex;
    flex-direction: row;
  }

  .about-text {
    display: flex;
    flex-direction: column;
    justify-content: center;
    margin: 0;
  }

  img {
    width: 200px;
    margin: 1rem;
  }
}

@media only screen and (max-width: 600px) {
  img {
    width: 200px;
    margin-bottom: 2rem;
  }

  .about-content {
    flex-direction: column;
  }

  .about-text {
    font-size: 10px;
    line-height: 18px;
    margin: 0;
  }

  .mobile-hidden {
    display: none;
  }
}

@media only screen and (max-width: 350px) {
  .about-content {
    flex-direction: column;
  }

  .about-text {
    font-size: 10px;
    line-height: 15px;
    width: 100%;
    margin: 0;
  }

  img {
    display: none;
  }
}
</style>
