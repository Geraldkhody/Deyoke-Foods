<template>
  <div id="about">
    <AboutComponent 
        v-for="(item, index) in aboutList" 
        :title="item.title" 
        :body="item.body"
        :key="index"
    />
    <Aims />
  </div>
</template>

<script setup>
import { reactive } from "vue";
import AboutComponent from "./AboutComponent/AboutComponent.vue";
import Aims from "./Aims/Aims.vue";


const aboutList = reactive([
  {
    title: "ABOUT US",
    body: "Deyoke Foods is an innovator in turkey berry powder and tea, transforming this sector and elevating these super foods to height. We deliver premium organic and high-quality turkey berry powder and tea crafted in different flavors perfectly for domestic and industrial purposes such as pharmaceuticals, cosmetics, culinary uses, traditional medicines, and everyone who needs natural energy and immune booster for a healthy lifestyle.",
  },
  {
    title: "Our Mission",
    body: "Deyoke Foods' mission is to empower individuals to lead healthier lives by providing high-quality, nutritious turkey berry powder and tea. We are committed to sustainable practices that support local communities and the environment, while educating consumers about the benefits of our products. Through innovation and a focus on quality, we aim to inspire a wellness-focused lifestyle, making natural health accessible to everyone.",
  },
  {
    title: "Our Vision",
    body: "Deyoke Foods envisions a world where nutritious, natural products enhance everyday wellness. By specializing in the production of turkey berry powder and tea, we aim to promote holistic health and sustainable living. Our commitment is to source high-quality ingredients, maintain eco-friendly practices, and empower communities through education about the benefits of turkey berry. We strive to be a leader in the health food industry, inspiring consumers to embrace wholesome choices that support their well-being and the environment.",
  },
]);
</script>

<style scoped>
#about {
  margin-top: 5rem;
  margin-bottom: 5rem;
}
</style>
