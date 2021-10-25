<template>
  <div class="home">
    <Nav />
    <div class="image">
      <img src="../images/henrikmainpic.png" alt="" />
    </div>
  </div>
</template>

<script>
// @ is an alias to /src
import Nav from "@/components/Nav.vue";

export default {
  name: "Home",
  components: {
    Nav,
  },
};
</script>

<style scoped>
body {
  overflow: hidden;
}

.image {
  display: flex;
  position: absolute;
  left: 50%;
  top: 50%;
  transform: translate(-50%, -50%);
}
img {
  height: 600px;
}

@media only screen and (max-width: 600px) {
  img {
    height: 300px;
  }
}
</style>
