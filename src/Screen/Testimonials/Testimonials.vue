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
        body: '"I’ve been incorporating Deyoke Foods’ turkey berry powder into my morning smoothies, and the difference is incredible! I feel more energized throughout the day, and I love knowing I’m adding such a nutritious ingredient to my diet. The flavor is subtle yet delightful, and I can’t recommend it enough!"',
        user: "Sarah Mensah",
    },
])

</script>

<style  scoped>
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
  gap: 13rem;
  margin-top: 1.5rem;
  justify-content: center;
}

</style>