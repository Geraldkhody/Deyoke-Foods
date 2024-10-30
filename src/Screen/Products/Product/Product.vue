<template>
  <div class="product">
    <div class="header-section">
        <Container>
      <div class="header-text">
        <h1>Deyoke Foods Turkey Berry Products</h1>
        <p class="subheading">SHOP</p>
        <p>OUR GLOBAL OUTLET</p>
        <p>All across Ghana and other countries we ship and deliver.</p>
        <ul class="benefits">
          <li>Proteins</li>
          <li>Fibres</li>
          <li>Vitamins A, C</li>
          <li>Minerals</li>
          <li>Antioxidants</li>
          <li>Carbohydrates, etc</li>
        </ul>
      </div>
      <div class="header-image">
        <img src="@/assets/product.jpg" alt="Turkey Berry Product" />
      </div>
        </Container>
    </div>
  </div>
</template>

<script setup>
import Container from "@/components/Container/Container.vue"

</script>

<style scoped>
.header-section {
    padding: 3rem 0;
  background-color: #e6f0e6;
}

.container {
    align-items: center;
    display: flex;
    /* justify-content: space-between; */
    gap: 10rem;
}

.header-text h1 {
  font-size: 2rem;
  font-weight: bold;
  color: #0f3c4b;
}

.header-text .subheading {
  font-weight: bold;
  color: #0f3c4b;
}

.header-text p {
  margin: 0.5rem 0;
}

.header-text .benefits {
  list-style: none;
  padding: 0;
  margin: 1rem 0;
}

.header-text .benefits li {
  margin: 0.5rem 0;
}

.header-image img {
  width: 400px;
  border-radius: 8px;
}
</style>
