<template>
    <div class="product-section" style="background-color: #fdf3d6;">
        <Container>
      <div class="product-info">
        <h2>Turkey Berry Powder</h2>
        <p>
          Turkey berry powder can be used as both food and herbal remedy for countless physical ailments,
          including high blood pressure, digestive issues, bacterial infections, and more.
        </p>
        <div class="buttons">
          <button class="primary-btn">Purchase product</button>
          <button class="secondary-btn">Read more</button>
        </div>
      </div>
      <div class="product-image">
        <img src="@/assets/powder.jpg" alt="Turkey Berry Powder" />
      </div>
        </Container>

    </div>

</template>

<script setup>
import Container from "@/components/Container/Container.vue"


</script>

<style scoped>


.product-section {
    padding: 2rem;
}

.container {
    justify-content: space-between;
    align-items: center;
    display: flex;
    gap: 10rem;
    
}

.product-info h2 {
  font-size: 1.5rem;
  font-weight: bold;
  color: #0f3c4b;
}

.product-info p {
  margin: 1rem 0;
}

.buttons {
  margin-top: 1rem;
}

.primary-btn,
.secondary-btn {
  padding: 0.5rem 1rem;
  border: none;
  cursor: pointer;
  border-radius: 4px;
}

.primary-btn {
  background-color: #0f3c4b;
  color: #fff;
  margin-right: 0.5rem;
}

.secondary-btn {
  background-color: transparent;
  color: #0f3c4b;
  border: 1px solid #0f3c4b;
}

.product-image img {
  max-width: 100%;
  border-radius: 8px;
}

.testimonials-section {
  padding: 2rem;
  text-align: center;
}

.testimonials-section h2 {
  font-size: 2rem;
  font-weight: bold;
  color: #0f3c4b;
  margin-bottom: 1.5rem;
}

.testimonials {
  display: flex;
  gap: 1rem;
  justify-content: center;
}

.testimonial {
  max-width: 400px;
  background-color: #f9f9f9;
  padding: 1rem;
  border-radius: 8px;
  text-align: left;
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
</style>
