<template>
  <div>
    <Nav />
    <div class="blog">
      <div class="blog-content">
        <h4>title</h4>
        <p>
          Lorem ipsum dolor, sit amet consectetur adipisicing elit. Dolore
          dolorum quae maxime ullam porro dicta voluptate expedita nostrum
          aperiam. Necessitatibus dolorem nostrum ipsam ea id possimus dolor
        </p>
        <a href="wordpress.com"><p>read more</p></a>
        <h4>title</h4>
        <p>
          Lorem ipsum dolor, sit amet consectetur adipisicing elit. Dolore
          dolorum quae maxime ullam porro dicta voluptate expedita nostrum
          aperiam. Necessitatibus dolorem nostrum ipsam ea id possimus dolor
        </p>
        <a href="wordpress.com"><p>read more</p></a>
        <h4>title</h4>
        <p>
          Lorem ipsum dolor, sit amet consectetur adipisicing elit. Dolore
          dolorum quae maxime ullam porro dicta voluptate expedita nostrum
          aperiam. Necessitatibus dolorem nostrum ipsam ea id possimus dolor
        </p>
        <a href="wordpress.com"><p>read more</p></a>
      </div>
    </div>
  </div>
</template>

<script>
import Nav from "../components/Nav.vue";
export default {
  name: "Blog",
  components: { Nav },
};
</script>

<style scoped>
.blog {
  position: fixed;
  top: 50%;
  left: 50%;
  transform: translate(-50%, -50%);
  font-size: 12px;
}

.blog-grid {
  display: grid;
  justify-content: flex-start;
  align-items: center;
  grid-auto-columns: 1fr 1fr;
}

.left {
  grid-column: 1;
}

.right {
  grid-column: 2;
}
</style>
