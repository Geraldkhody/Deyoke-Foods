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
  font-size: 2rem;
  font-weight: bold;
  color: var(--primary-color);
}

.product-info p {
  margin: 1rem 0;
  line-height: 1.5;
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
  background-color: var(--primary-color);
  color: #fff;
  margin-right: 0.5rem;
}

.secondary-btn {
  background-color: transparent;
  color: #0f3c4b;
  border: 1px solid var(--primary-color);
}

.product-image {
  border-radius: 8px;
  width: 1000px;
}

.product-image img {
  width: 100%;
  height: 100%;
  object-fit: cover;
}


@media (max-width: 1023px) {

}

@media (max-width: 768px) {
  .container {
    flex-direction: column;
    gap: 2rem;
  }

  .product-image {
    width: 90%;
  }
}

</style>
