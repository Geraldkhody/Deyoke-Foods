<template>
  <div>
    <div class="product-section" style="background-color: #eaf4f4">
      <Container>
        <div class="product-image">
          <img src="@/assets/tea.jpg" alt="Turkey Berry Tea" />
        </div>
        <div class="product-info">
          <h2>Turkey Berry Tea</h2>
          <p>
            Turkey berry powder as tea can be mixed with other herbs. It is a
            good source of iron, gingerol, fibre and antioxidants which helps in
            preventing high blood sugar and maintains blood sugar balance.
          </p>
          <button class="secondary-btn">Learn more</button>
        </div>
      </Container>
    </div>
  </div>
</template>

<script setup>
import Container from "@/components/Container/Container.vue";
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

.product-image img {
  width: 100%;
  border-radius: 8px;
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
</style>
