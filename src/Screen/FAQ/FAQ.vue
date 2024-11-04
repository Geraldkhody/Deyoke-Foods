<template>
  <div id="faq" class="faq-section">
    <Container>
      <p class="header">Frequently Asked Questions</p>
      <div>
        <Question 
          v-for="(item, index) in faqItems"
          :key="index"
          :index="item.index"
          :question="item.question"
          :answer="item.answer"
        />
      </div>
    </Container>
  </div>
</template>

<script setup>
import { ref } from "vue";
import Container from "@/components/Container/Container.vue";
import Question from "./Question.vue"


const faqItems = [
  {
    question: "Can pregnant women take our products?",
    answer:
      "Yes, pregnant women can take our turkey berry powder and tea, as turkey berry is known for its nutritional benefits. However, we always recommend consulting with a healthcare provider before adding any new supplements or herbal products to ensure they align with individual health needs and circumstances during pregnancy. Your health and safety are our top priorities.",
  },
  {
    question:
      "How can incorporating turkey berry powder into my diet benefit my overall health?",
    answer:
      "Incorporating turkey berry powder into your diet can offer numerous health benefits. It is rich in essential vitamins and minerals, including vitamins A and C, calcium, and iron. These nutrients can help boost your immune system, support healthy skin, and improve bone health. Additionally, turkey berry is known for its antioxidant properties, which can help combat oxidative stress in the body. Regular consumption may also aid in digestion and promote overall wellness, making it a great addition to smoothies, soups, or teas.",
  },
];


</script>

<style scoped>
.faq-section {
  width: 100%;
  margin-top: 6rem;
  padding: 2rem;
  background-color: #f5f8f6;
}

.container {
  /* display: flex; */
  justify-content: space-between;
  width: 70%;
  gap: 3rem;
}

.header {
  text-align: center;
}

p {
  font-size: 2rem;
  margin-bottom: 1rem;
  color: #333;
  font-weight: 100;
}



@media (max-width: 1024px) {
  .container {
    /* flex-direction: column; */
  }
  .faq-section {
    padding: 1.5rem;
  }

  p {
    font-size: 1.8rem;
  }
}

@media (max-width: 768px) {
  .faq-section {
    padding: 1rem;
  }

  p {
    font-size: 1.6rem;
  }

  .faq-question {
    font-size: 1rem;
  }

  .arrow {
    font-size: .8rem;
  }

  .faq-answer {
    font-size: 0.9rem;
  }
}

@media (max-width: 480px) {
  .container {
    width: 85%;
  }

  .faq-section {
    padding: 0.5rem;
  }

  p {
    font-size: 1.4rem;
  }
}
</style>
