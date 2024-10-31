<template>
    <Container>
      <h2>Testimonials</h2>
      <div class="testimonials">
        <Testimonial 
          v-for="(item, index) in testimonials"
          :key="index"
          :body="item.body"
          :user="item.user"
        />
      </div>
    </Container>
</template>

<script setup>
import Container from "@/components/Container/Container.vue"
import { reactive } from "vue"
import Testimonial from "./Testimonial.vue"

const testimonials = reactive([
    {
        body: '"I’ve been incorporating Deyoke Foods’ turkey berry powder into my morning smoothies, and the difference is incredible! I feel more energized throughout the day, and I love knowing I’m adding such a nutritious ingredient to my diet. The flavor is subtle yet delightful, and I can’t recommend it enough!"',
        user: "Sarah Mensah",
    },
    {
        body: `"Deyoke Foods' turkey berry tea has become my go-to evening ritual. It’s calming and delicious, and I appreciate its health benefits. I've noticed improved digestion and a boost in my overall well-being since I started drinking it regularly. It’s a perfect way to unwind after a long day!"`,
        user: "James Oppong",
    },
])
</script>

<style scoped>
.container {
  margin-top: 4rem;
}

h2 {
  font-size: 2rem;
  font-weight: bold;
  color: #0f3c4b;
  text-align: center;
}

.testimonials {
  display: flex;
  gap: 3rem;
  margin-top: 1.5rem;
  justify-content: center;
  flex-wrap: wrap;
}

/* Responsive styling */
@media (max-width: 1023px) {
  h2 {
    font-size: 1.75rem;
  }
  .testimonials {
    gap: 2rem;
  }
}

@media (max-width: 768px) {
  h2 {
    font-size: 1.5rem;
  }
  .testimonials {
    flex-direction: column;
    align-items: center;
  }
}
</style>
