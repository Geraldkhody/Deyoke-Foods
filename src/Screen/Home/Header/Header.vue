<template>
  <div id="header">
    <div class="background">
      <img src="@/assets/home_background.jpg" alt="" />
    </div>
    <div class="over">
      <!-- <Navbar /> -->
      <Main />
      <Subscribe />
    </div>
  </div>
</template>

<script setup>
// import Navbar from "./Navbar.vue"
import Main from "./Main.vue"
import Subscribe from "./Subscribe.vue"


</script>

<style scoped>
#header {
    width: 100%;
    height: calc(100vh - var(--navbar-height));
    display: flex;
    justify-content: space-between;
    align-items: center;
    position: relative;
}

img {
    width: 100%;
    height: 100%;
    object-fit: cover;
    overflow: hidden;
}

.background {
    width: 100%;
    height: 100%;
}

.over {
    position: absolute;
    top: 0;
    left: 0;
    width: 100%;
    height: 100%;
    background-color: rgba(0, 0, 0, 0.7);
    z-index: 100;
    display: flex;
    flex-direction: column;
}
</style>
