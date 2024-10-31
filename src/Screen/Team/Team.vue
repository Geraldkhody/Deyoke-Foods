<template>
  <div class="wrapper">
    <h2>Team</h2>
  <Container>
    <div class="team-grid">
      <TeamMember
        v-for="member in team"
        :key="member.name"
        :image="member.image"
        :role="member.role"
        :degree="member.degree"
        :name="member.name"
        :single="member.single"
      />
    </div>
      <CEOMember
        :key="ceo.name"
        :image="ceo.image"
        :role="ceo.role"
        :degree="ceo.degree"
        :name="ceo.name"
        :single="ceo.single"
      />
  </Container>
    </div>
</template>

<script setup>
import { ref } from 'vue';
import TeamMember from './TeamMember/TeamMember.vue';
import CEOMember from './TeamMember/CEOMember.vue';
import Container from '@/components/Container/Container.vue';



    const team = ref([
      {
        
        image: require('@/assets/Emmanuel.jpg'),
        role: 'Communication & Quality Assurance Lead',
        degree: 'Bsc. Agricultural Engineering',
        name: 'Emmanuel Adjei',
      },
      {
        image: require('@/assets/Victoria.jpg'),
        role: 'Marketing & Finance Lead',
        degree: 'Bsc. Entrepreneurship',
        name: 'Baffour Frimpong Victoria',
      },
      {
        image: require('@/assets/Martin.jpg'),
        role: 'Chief Operations Officer (co-founder)',
        degree: 'Bsc. Mechanical Engineering',
        name: 'Martin Atampugre',
      },
    ]);

    const ceo = ref({
        image: require('@/assets/Joshua.jpg'),
        role: 'CEO, Production Lead (Founder)',
        degree: 'Bsc. Agricultural Engineering',
        name: 'Akanzige Tanga Joshua',
    })

</script>

<style scoped>
h2 {
  text-align: center;
}

.wrapper {
  text-align: center;
  margin-top: 6rem;
}

.team-grid {
  display: grid;
  grid-template-columns: repeat(3, 1fr);
  gap: 4rem;
  margin-top: 2rem;
}

/* Responsive Styling */
@media (max-width: 1023px) {
    .team-grid {
      grid-template-columns: 1fr 1fr;
      gap: 2.5rem;
    }
}


@media (max-width: 767px) {
  .container {
    display: flex;
    flex-direction: column-reverse;
  }

  .team-grid {
    display: flex;
    flex-direction: column-reverse;
    
    gap: 2rem;
  }
}


</style>
