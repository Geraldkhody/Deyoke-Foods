<template>
  <div class="faq-item">
    <div class="faq-question" @click="toggle(index)">
      <span>{{ question }}</span>
      <span class="arrow">{{ openIndex === index ? "▲" : "▼" }}</span>
    </div>
    <div v-if="openIndex === index" class="faq-answer">
      <p>{{ answer }}</p>
    </div>
  </div>
</template>

<script setup>
import { defineProps, ref } from "vue"

const props = defineProps(["index", "question", "answer"])

// State to track which question is open
const openIndex = ref(null);

// Function to toggle the answer visibility
const toggle = (index) => {
  openIndex.value = openIndex.value === index ? null : index;
};

</script>

<style scoped>
.faq-item {
  border-bottom: 1px solid #ddd;
  padding: 0.5rem 0;
  /* display: flex; */
}

.faq-question {
  display: flex;
  justify-content: space-between;
  align-items: center;
  font-weight: bold;
  cursor: pointer;
  padding: 0.5rem 0;
  /* gap: 1rem; */
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
  p {
    font-size: 1.8rem;
  }
}

@media (max-width: 768px) {

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

  .faq-question {
    font-size: 0.9rem;
    align-items: flex-start;
    padding-bottom: 0.3rem;
  }

  .arrow {
    font-size: 0.9rem;
    margin-left: 1rem;
  }

  .faq-answer {
    font-size: 7rem;
  }

  .faq-answer p {
    font-size: 0.8rem;
    line-height: 1.4;
    padding-top: 0.2rem;
  }

}

</style>
