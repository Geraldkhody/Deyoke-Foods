<template>
  <div class="ceo-member">
    <MemberDetails 
        :role="role" 
        :name="name"
        :degree="degree"
    />
    <div class="profile-image">
      <img :src="image" :alt="`Profile picture of ${name}`" class="ceo-image" />
    </div>
  </div>
</template>

<script setup>
import MemberDetails from "./MemberDetails.vue"
import { defineProps } from "vue"

const props = defineProps({
  image: String,
  role: String,
  degree: String,
  name: String,
})
</script>

<style scoped>
.member-details {
    margin: 3rem 8rem;
}

/* .member-details .member-name {
    font-size: 5rem;
} */

.ceo-member {
  display: flex;
  flex-direction: row;
  text-align: left;
  margin: 1rem;
  margin-top: 2rem;
  transition: transform 0.2s ease-in-out;
  border: 1px solid #E1E5F0;
  border-radius: 10px;
}

.ceo-member:hover {
  transform: scale(1.02);
}

.profile-image {
  width: 45%;
  height: 350px;
  border-radius: 8px;
  overflow: hidden;
  margin-left: auto;
}

.ceo-image {
  width: 100%;
  height: 100%;
  object-fit: cover;
  object-position: top; /* Adjust to show the top part of the image */
}

/* Responsive styling */
@media (max-width: 1023px) {
  .member-details {
    margin: 3rem 8rem;
  }

  .ceo-member {
    flex-direction: column-reverse  ;
    align-items: center;
    text-align: center;
    width: 80%;
    justify-content: center;
  }
  .profile-image {
    width: 100%;
    height: 380px;
  }
}

@media (max-width: 768px) {
  .member-details {
    margin: 1rem 0;

  }

  .ceo-member {
    flex-direction: column-reverse;
    align-items: center;
    width: 100%;
    margin: 0;
  }
  .profile-image {
    width: 100%;
    height: 380px;
  }
}
</style>
