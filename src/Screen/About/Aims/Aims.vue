<template>
  <Container >
    <div class="aims-grid">
      <AimCard
        v-for="(item, index) in aimsList"
        :key="index"
        :icon="item.icon"
        :title="item.title"
        :description="item.description"
      />
      
    </div>
  </Container>
</template>

<script setup>
import { reactive } from 'vue'
import AimCard from './AimCard.vue'
import Container from "@/components/Container/Container.vue"


const aimsList = reactive([
  { 
    icon: require('@/assets/core icons/recruitment.svg'), 
    title: 'Promote Health and Wellness', 
    description: 'Provide high-quality turkey berry powder and tea that enhance nutritional intake and support overall well-being.' 
  },
  { 
    icon: require('@/assets/core icons/employees.svg'), 
    title: 'Educate Consumers', 
    description: 'Raise awareness about the benefits of turkey berry and its role in traditional medicine and modern nutrition.' 
  },
  { 
    icon: require('@/assets/core icons/trainings.svg'), 
    title: 'Sustainability', 
    description: 'Implement eco-friendly practices throughout our production processes to minimize environmental impact.' 
  },
  { 
    icon: require('@/assets/core icons/sales.svg'), 
    title: 'Support Local Communities', 
    description: 'Collaborate with local farmers and producers, fostering economic growth and sustainable agriculture.' 
  },
  { 
    icon: require('@/assets/core icons/customer-service.svg'), 
    title: 'Innovation', 
    description:"Continuously develop new products and formulations that meet evolving consumer needs while maintaining the integrity of our ingredients."
  },
  { 
    icon: require('@/assets/core icons/safety.svg'),
    title:"Quality Assurance",
    description:"Maintain the highest standards of quality and safety in our products to build trust and loyalty among consumers."
  },
])

</script>

<style scoped>
.container {
  color: #fff;
  padding: 3rem 0;
  text-align: center;
  width: 70%;
  margin-top: 3rem;
}

.aims-grid {
  display: grid;
  grid-template-columns: repeat(3, 1fr);
  gap: 2.5rem;
}

.aims-title {
  font-size: 2rem;
  font-weight: 600;
  color: #014751;
  margin-bottom: 2.5rem;
}


@media (max-width: 1023px) {
  .container {
    width: 75%;
  }

  .aims-grid {
    grid-template-columns: 1fr 1fr;
  }
}

@media (max-width: 640px) {
  .container {
    width: 80%;
  }

  .aims-grid {
    grid-template-columns: 1fr;
  }
}

</style>