<template>
  <Home />
  <About />
</template>

<script>
import Home from "@/Screen/Home/Home.vue"
import About from "@/Screen/About/About.vue"

export default {
  name: 'App',
  components: {
    Home,
    About,
  }
}
</script>


<style>
:root {
  --container-width: 80%;
  --primarry-color: #014751;
  --light-green: #9FE82B;
  --dark-green: #083F3D;
  --text-green: #445D65;

}

* {
  margin: 0;
  padding: 0;
  box-sizing: border-box;
  font-family:  sans-serif;
}

#app {
  margin: auto;
}
</style>
