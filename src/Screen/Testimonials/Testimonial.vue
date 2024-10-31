<template>
    <div class="testimonials-section">
      <div class="testimonials">
        <div class="testimonial">
          <div class="header">
            <h3>Testimonial 2</h3>
            <img src="@/assets/Flower.svg" alt="">
          </div>
          <p class="body">
            {{ body }}
          </p>
          <small class="user"> — {{user}}</small>
        </div>
      </div>
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
}

.testimonial .header {
  display: flex;
  justify-content: space-between;
}

.testimonial .header img {
  width: 1.1rem;
}

.testimonial h3 {
  font-size: 1.25rem;
  font-weight: bold;
  color: #0f3c4b;
}

.testimonial p {
  color: #555;
  margin-top: 0.5rem;
}

.testimonial .body {
  font-style: italic;
}
</style>
