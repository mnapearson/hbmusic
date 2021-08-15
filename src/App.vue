<template>
  <div id="app">
    <div class="audio" @click="changeOff" :class="isOn ? 'isOn' : 'isOff'">
      <img src="./assets/soundbutton.svg" alt="" />
    </div>
    <audio
      preload="auto"
      loop
      id="audio"
      :src="require('./assets/henriktune.wav')"
    ></audio>
    <router-view class="view" />
  </div>
</template>

<script>
export default {
  data() {
    return {
      isOn: true,
    };
  },
  methods: {
    changeOff() {
      let oAudio = document.querySelector("#audio");
      if (this.isOn) {
        oAudio.play(); //Let the audio file start playing
      } else {
        oAudio.pause(); //Make the audio file pause
      }
      this.isOn = !this.isOn;
    },
    audioAutoPlay() {
      let audio = document.getElementById("audio");
      this.isOff = false;
      audio.play();
      document.removeEventListener("touchstart", this.audioAutoPlay);
    },
  },
  mounted() {
    this.audioAutoPlay("audio");
    // Automatically play music effects, solve the WeChat automatic playback problem
    document.addEventListener("touchstart", this.audioAutoPlay, false);
    document.addEventListener("WeixinJSBridgeReady", this.audioAutoPlay, false);
    let oAudio = document.querySelector("#audio");
    oAudio.onended = function () {
      //play is finished, replay loop
      oAudio.load();
      oAudio.play();
    };
  },
};
</script>

<style>
* {
  font-family: -apple-system, BlinkMacSystemFont, "Segoe UI", Roboto, Oxygen,
    Ubuntu, Cantarell, "Open Sans", "Helvetica Neue", sans-serif;
}

.audio img {
  width: 20px;
  height: 20px;
}

.audio {
  position: fixed;
  right: 0;
  top: 0;
  margin: 1rem;
}
</style>
