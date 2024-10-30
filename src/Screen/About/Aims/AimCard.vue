<template>
  <div class="aim-card">
    <div class="aim-icon"><img :src="icon" :alt="title"></div>
    <h3 class="aim-card-title">{{ title }}</h3>
    <p class="aim-card-description">{{ description }}</p>
  </div>
</template>

<script setup>
import { defineProps } from "vue"


const props = defineProps({
  icon: {
    type: String,
    required: true,
  },
  title: {
    type: String,
    required: true,
  },
  description: {
    type: String,
    required: true,
  },
})
</script>

<style scoped>
.aim-card {
  padding: 3rem 2rem;
  border: 1px solid #EAEEF2;
  border-radius: 0.5rem;
  text-align: left;
}

.aim-icon {
  width: 60px;
  margin-bottom: 1rem;
}

.aim-icon img {
  width: 100%;
  height: 100%;
  object-fit: cover;
}

.aim-card-title {
  font-size: 1.35rem;
  font-weight: 600;
  color: var(--primary-color);
  }

.aim-card-description {
  color: var(--primary-color);
  line-height: 1.2;
}

</style>
