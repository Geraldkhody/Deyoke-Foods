<template>
  <div class="wrapper">
    <Container>
      <hr />
      <div class="footer-content">
        <div class="footer-links">
          <p>Privacy Policy</p>
          <p>Privacy Settings</p>
          <p>Advertising Policy</p>
          <p>Health Topics</p>
          <p>Sponsor</p>
        </div>
        <div class="footer-contact">
          <p><strong>CONTACT Us</strong></p>
          <p>+233 544546153</p>
          <p>+233 508746143</p>
          <p>+233 503488172</p>
          <p>+233 530405497</p>
          <p>Email: deyoke.foods24@gmail.com</p>
          <p>P. O. BOX 2242, SUNYANI</p>
        </div>
      </div>
      <div class="footer-bottom">
        <p>Copyright © Deyoke 2024. All rights reserved</p>
      </div>
    </Container>
  </div>
</template>

<script setup>
import Container from "@/components/Container/Container.vue"
</script>

<style scoped>
.wrapper {
  background-color: #f5f8f6;
}

.container {
  padding: 2rem;
  font-size: 0.9rem;
}

.footer-content {
  display: flex;
  gap: 8rem;
  text-align: left;
}

.footer-links,
.footer-contact {
  margin-bottom: 1rem;
  display: flex;
  flex-direction: column;
  color: #999;
}

.footer-links p,
.footer-contact p {
  margin: 0.5rem 0;
}

.footer-bottom {
  display: flex;
  flex-direction: column;
  align-items: center;
  gap: 1rem;
  text-align: center;
  margin-top: 1.5rem;
  font-size: 0.8rem;
  color: #666;
}

/* Responsive styling */
@media (max-width: 1024px) {
  .footer-content {
    gap: 4rem;
  }
}

@media (max-width: 768px) {
  .footer-content {
    flex-direction: column;
    align-items: center;
    text-align: center;
    gap: 2rem;
    margin-top: 2rem;
  }

  .footer-links, 
  .footer-contact {
    align-items: center;
  }

  .footer-bottom {
    font-size: 0.75rem;
  }
}

@media (max-width: 480px) {
  .container {
    padding: 1rem;
  }

  .footer-links p, 
  .footer-contact p {
    font-size: 0.85rem;
    margin: 0.25rem 0;
  }

  .footer-bottom {
    font-size: 0.7rem;
  }
}
</style>
