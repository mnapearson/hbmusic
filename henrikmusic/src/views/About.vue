<template>
  <div class="about">
    <Nav />
    <div class="about-content">
      <div class="about-text">
        <p>
          Lorem ipsum dolor, sit amet consectetur adipisicing elit. Voluptates
          quos animi provident, asperiores quasi, nesciunt velit rem architecto
          fugit officia sit tempore. Deserunt sapiente velit, dolores explicabo
          quaerat ipsum officiis vero officia, nostrum placeat voluptatibus
          vitae architecto, dolor eveniet repellat laboriosam voluptatum omnis
          provident natus soluta tempora et! Sed magnam reprehenderit harum
          omnis, quae perferendis, quos quaerat soluta nemo ratione dolor
          voluptatum. Dolores, fugit sed consequuntur laboriosam vitae ullam
          nemo animi nulla, rem, fugiat cumque saepe. Nam illum sequi doloremque
          suscipit tempora? Maxime architecto cupiditate ipsa et aperiam,
          veritatis nihil, veniam, hic impedit beatae eveniet numquam provident
          nostrum quam deserunt!
        </p>
        <p>
          Dolores, fugit sed consequuntur laboriosam vitae ullam nemo animi
          nulla, rem, fugiat cumque saepe. Nam illum sequi doloremque suscipit
          tempora?
        </p>
      </div>
      <div class="about-carousel">
        <img src="../images/henrikslide1.png" alt="" />
        <img src="../images/henrikslide2.png" alt="" />
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
</style>
