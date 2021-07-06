<template>
  <div class="home">
    <Nav />
    <h1>home</h1>
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
