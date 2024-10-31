<template>
  <div class="team-member">
    <div class="profile-image">
      <img :src="image" :alt="`Profile picture of ${name}`" class="member-image" />
    </div>
    <MemberDetails 
        :role="role" 
        :name="name"
        :degree="degree"
    />
  </div>
</template>

<script setup>
import MemberDetails from "./MemberDetails.vue"
import {defineProps} from "vue"

const props = defineProps({
    image: String,
    role: String,
    degree: String,
    name: String,
})

</script>

<style scoped>
.team-member {
  display: flex;
  flex-direction: column;
  text-align: left;
  transition: transform 0.2s ease-in-out;
  width: 100%;
}

.team-member:hover {
  transform: scale(1.02);
}

.profile-image {
  width: 100%;
  height: 270px;
  margin-bottom: 1rem;
  border-radius: 8px;
  overflow: hidden;
}

.member-image {
  width: 100%;
  height: 100%;
  object-fit: cover;
}




/* Responsive styling */
@media (max-width: 1023px) {
    .team-member {
    width: 350px;
    /* height: 200px; */
  }
  
}

@media (max-width: 767px) {
  .team-member {
    width: 100%;
    display: grid;
    grid-template-columns: 1fr 1fr;
    gap: 2rem;
  }
  .profile-image {
    /* min-width: 200px; */
  }

  .member-details {
    margin-top: 2rem;
  }
}

@media (max-width: 610px) {
    .team-member {
        width: 100%;
        display: grid;
        grid-template-columns: 1fr;
        gap: 0.2rem;
    }
    .member-details {
        margin-top: 0;
        margin-left: 1rem;
        /* text-align: center; */
    }
}
</style>
