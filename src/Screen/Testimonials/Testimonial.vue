<template>
  <div class="testimonial">
    <div class="header">
      <h3>Testimonial</h3>
      <img src="@/assets/Flower.svg" alt="">
    </div>
    <p class="body">
      {{ body }}
    </p>
    <small class="user"> — {{ user }}</small>
  </div>
</template>

<script setup>
import { defineProps } from "vue"

const props = defineProps({
  body: {
    type: String,
    required: true
  },
  user: {
    type: String,
    required: true
  }
})
</script>

<style scoped>
.testimonial {
  max-width: 400px;
  background-color: #f9f9f9;
  padding: 1rem;
  border-radius: 8px;
  text-align: left;
  margin: 0.5rem;
}

.header {
  display: flex;
  justify-content: space-between;
}

.header img {
  width: 1.1rem;
}

h3 {
  font-size: 1.25rem;
  font-weight: bold;
  color: #0f3c4b;
}

.body {
  color: #555;
  margin-top: 0.5rem;
  font-style: italic;
}

.user {
  color: #777;
  font-size: 0.9rem;
  display: block;
  margin-top: 1rem;
}

/* Responsive styling */
@media (max-width: 768px) {
  .testimonial {
    max-width: 90%;
    padding: 1rem;
  }
  
  h3 {
    font-size: 1.1rem;
  }
  
  .body {
    font-size: 0.9rem;
  }
  
  .user {
    font-size: 0.8rem;
  }
}
</style>
