<template>
    <div class="member-details">
        <h4 class="member-role">{{ role }}</h4>
        <p class="member-name">{{ name }}</p>
        <h3 class="member-school">University of Energy and Natural Resources</h3>
        <p class="member-degree">{{ degree }}</p>
    </div>
</template>

<script setup>
import {defineProps} from "vue"

const props = defineProps({
    role: String,
    degree: String,
    name: String,
})

</script>

<style scoped>
.member-role {
  font-weight: bold;
  color: var(--primary-color);
  border: 1px solid #00D37F;
  border-radius: 5px;
  font-size: 0.75rem;
  padding: 2px 5px;
  margin-top: 5px;
  display: inline;
}

.member-name {
  font-size: 1.1rem;
  margin-top: 7px;
  margin-bottom: 2px;
  font-weight: bold;
  color: var(--primary-color);
}

.member-school {
  font-weight: normal;
  color: #666;
  font-size: 0.8rem;
  font-style: italic;
}

.member-degree {
    font-style: italic;
  font-size: 0.75rem;
  color: #666;

}

</style>