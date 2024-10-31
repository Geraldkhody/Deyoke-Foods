<template>
  <div class="product">
    <Container>
      <div class="product-content">
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
      <div class="product-image">
        <img src="@/assets/product.png" alt="Turkey Berry Product" />
      </div>
    </Container>
  </div>
</template>

<script setup>
import Container from "@/components/Container/Container.vue"

</script>

<style scoped>
.product {
    padding: 3rem 0;
  /* background-color: #e6f0e6; */
  /* height: 200px; */
}

.container {
    align-items: center;
    display: flex;
    gap: 10rem;
  }

.product-content {
  background-color: #fff;
  height: 100%;
  /* width: 50%; */
}

.product-content h1 {
  font-size: 2.1rem;
  font-weight: bold;
  color: #0f3c4b;
  margin-bottom: 2rem;
}

.product-content p {
  font-weight: bold;
  color: var(--primary-color);
  margin: 0.5rem 0;
  font-size: 14px;
}

.product-content .benefits {
  list-style: none;
  padding: 0;
  margin-top: 2rem ;
}

.product-content .benefits li {
  margin: 0.5rem 0;
}

.product-image {
  background-color: var(--primary-color);
  border-radius: 8px;
  padding: 1rem 2rem ;
  max-width: clamp(100%, 380px, 350px);
}

.product-image img {
  width: 100%;
  height: 100%;
  object-fit: cover;
}

@media (max-width: 768px) {
  .container {
    flex-direction: column;
    gap: 1rem;
  }

 
}
</style>
