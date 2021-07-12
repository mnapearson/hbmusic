<template>
  <div class="project-details">
    <Nav />
    <div class="project-main">
      <div class="project-left">
        <div class="project-description"></div>
        <div class="project-events"></div>
      </div>
      <div class="project-right"><div class="project-links"></div></div>
    </div>
    <div class="next-project">
      <router-link to="/projects">next project</router-link>
    </div>
  </div>
</template>

<script>
import Nav from "@/components/Nav.vue";

export default {
  name: "ProjectDetails",
  components: {
    Nav,
  },
};
</script>

<style scoped></style>
