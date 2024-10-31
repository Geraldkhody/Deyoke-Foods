<template>
  <div class="faq-section">
    <Container>
      <p class="header">Frequently Asked Questions</p>
      <div>
        <div v-for="(item, index) in faqItems" :key="index" class="faq-item">
          <div class="faq-question" @click="toggle(index)">
            <span>{{ item.question }}</span>
            <span class="arrow">{{ openIndex === index ? "▲" : "▼" }}</span>
          </div>
          <div v-if="openIndex === index" class="faq-answer">
            <p>{{ item.answer }}</p>
          </div>
        </div>
      </div>
    </Container>
  </div>
</template>

<script setup>
import { ref } from "vue";
import Container from "@/components/Container/Container.vue";

// Data for the FAQ items
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

// State to track which question is open
const openIndex = ref(null);

// Function to toggle the answer visibility
const toggle = (index) => {
  openIndex.value = openIndex.value === index ? null : index;
};
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

p {
  font-size: 2rem;
  margin-bottom: 1rem;
  color: #333;
  font-weight: 100;
}

.faq-item {
  border-bottom: 1px solid #ddd;
  padding: 0.5rem 0;
}

.faq-question {
  display: flex;
  justify-content: space-between;
  align-items: center;
  font-weight: bold;
  cursor: pointer;
  padding: 0.5rem 0;
}

.arrow {
  font-size: 1.2rem;
  color: #666;
  margin-left: 2rem;
}

.faq-answer p {
  padding: 0.5rem 0;
  color: #555;
  font-size: 1rem;
  margin-left: 1rem;
}

@media (max-width: 1024px) {
  .container {
    flex-direction: column;
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
    font-size: 1rem;
  }

  .faq-answer {
    font-size: 1rem;
  }
}

@media (max-width: 480px) {
  .faq-section {
    padding: 0.5rem;
  }

  p {
    font-size: 1.4rem;
  }

  .faq-question {
    font-size: 0.9rem;
    flex-direction: column;
    align-items: flex-start;
  }

  .arrow {
    font-size: 0.9rem;
    margin-left: 0;
  }

  .faq-answer {
    font-size: 0.8rem;
  }
}
</style>
