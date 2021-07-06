<template>
  <div class="nav-main">
    <nav>
      <div class="audio" @click="changeOn" :class="isOff ? 'isOff' : 'isOn'">
        <img src="../assets/soundbutton.svg" alt="" />
      </div>
      <audio
        preload="auto"
        loop
        id="audio"
        :src="require('../assets/leo.wav')"
      ></audio>

      <div class="top">
        <router-link class="link" to="/">Henrik Baumgarten</router-link>
      </div>
      <div class="left">
        <router-link class="link" to="/about">About</router-link>
      </div>
      <div class="bottom">
        <router-link class="link" to="/contact">Contact</router-link>
      </div>
      <div class="right">
        <router-link class="link" to="/projects">Projects</router-link>
      </div>
    </nav>
  </div>
</template>

<script>
export default {
  name: "Nav",
  data() {
    return {
      isOff: true,
    };
  },
  methods: {
    changeOn() {
      let oAudio = document.querySelector("#audio");
      if (this.isOff) {
        oAudio.play(); //Let the audio file start playing
      } else {
        oAudio.pause(); //Make the audio file pause
      }
      this.isOff = !this.isOff;
    },
    audioAutoPlay() {
      let audio = document.getElementById("audio");
      this.isOff = false;
      audio.play();
      document.removeEventListener("touchstart", this.audioAutoPlay);
    },
  },
  // mounted() {
  //   this.audioAutoPlay("audio");
  //   // Automatically play music effects, solve the WeChat automatic playback problem
  //   document.addEventListener("touchstart", this.audioAutoPlay, false);
  //   document.addEventListener("WeixinJSBridgeReady", this.audioAutoPlay, false);
  //   let oAudio = document.querySelector("#audio");
  //   oAudio.onended = function () {
  //     //play is finished, replay loop
  //     oAudio.load();
  //     oAudio.play();
  //   };
  // },
};
</script>

<style scoped>
.audio img {
  width: 20px;
  height: 20px;
}

.audio {
  position: fixed;
  right: 0;
  margin-right: 2rem;
}

.link {
  text-decoration: none;
  text-transform: uppercase;
  color: black;
  font-size: 12px;
}
.top {
  position: fixed;
  top: 0;
  right: 43%;
  margin: 1rem;
}
.top .link:hover,
.top .router-link-exact-active {
  color: purple;
  font-weight: bold;
}

.left {
  position: fixed;
  left: 0;
  top: 50%;
  margin: 1rem;
  transform: rotate(-90deg);
}

.left .link:hover,
.left .router-link-active {
  color: orange;
  font-weight: bold;
}
.bottom {
  position: fixed;
  bottom: 0;
  right: 47%;
  margin: 1rem;
}
.bottom .link:hover,
.bottom .router-link-active {
  color: red;
  font-weight: bold;
}

.right {
  position: fixed;
  right: 0;
  top: 50%;
  margin: 1rem;
  transform: rotate(90deg);
}
.right .link:hover,
.right .router-link-active {
  color: green;
  font-weight: bold;
}
</style>
