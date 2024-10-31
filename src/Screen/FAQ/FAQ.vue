<template>
  <div class="faq-section">
    <Container>
    <p>Frequently Asked Questions</p>
    <div>
        <div v-for="(item, index) in faqItems" :key="index" class="faq-item">
        <div 
            class="faq-question" 
            @click="toggle(index)"
        >
            <span>{{ item.question }}</span>
            <span class="arrow">{{ openIndex === index ? '▲' : '▼' }}</span>
        </div>
        <div 
            v-if="openIndex === index" 
            class="faq-answer"
        >
            <p>{{ item.answer }}</p>
        </div>
        </div>

    </div>
    </Container>
  </div>
</template>

<script setup>
import { ref } from 'vue'
import Container from "@/components/Container/Container.vue"

// Data for the FAQ items
const faqItems = [
  { question: 'Can pregnant women take our products?', answer: 'Our products are natural, but we recommend consulting a healthcare provider before use during pregnancy.' },
  { question: 'How can incorporating turkey berry powder into my diet benefit my overall health?', answer: 'Turkey berry powder is rich in nutrients and can support immune health, digestion, and energy levels.' },
  { question: 'Turkey berry and fertility', answer: 'Turkey berry has been traditionally used for its potential fertility-boosting properties.' },
  { question: 'How to use turkey berry to treat anemia', answer: 'Turkey berry is rich in iron and can help improve anemia when consumed as part of a balanced diet.' },
  { question: 'Turkey berry spiritual benefits', answer: 'Turkey berry is believed to have protective and healing spiritual qualities in various cultures.' },
  { question: 'What is the use of turkey berry plant?', answer: 'Turkey berry can be used for culinary, medicinal, and nutritional purposes.' },
  { question: 'How to take turkey berry powder', answer: 'Turkey berry powder can be added to smoothies, soups, or sprinkled on meals for added nutrition.' },
  { question: 'Turkey berry side effects', answer: 'While generally safe, excessive consumption may cause stomach upset. Consult a doctor if you experience any adverse effects.' }
]

// State to track which question is open
const openIndex = ref(null)

// Function to toggle the answer visibility
const toggle = (index) => {
  openIndex.value = openIndex.value === index ? null : index
}
</script>

<style scoped>
.faq-section {
  width: 100%;
  margin-top: 6rem;
  padding: 2rem;
  background-color: #f5f8f6;
}

.container {
  display: flex;
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

.faq-answer {
  padding: 0.5rem 0;
  color: #555;
  font-size: 0.9rem;
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
    font-size: 0.85rem;
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
