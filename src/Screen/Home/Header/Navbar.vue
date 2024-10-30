<template>
  <nav :class="{ scrolled: isScrolled }">
    <Container>
      <div class="logo">
        <a href="#home">
          <img src="@/assets/logo_new.png" alt="Logo">
        </a>
      </div>

      <!-- Main Links (visible on desktop and as a dropdown in mobile) -->
      <div :class="{ 'link': true, 'dropdown-menu': showMenu }">
        <a @click.prevent="scrollToSection('about')">About Us</a>
        <a @click.prevent="scrollToSection('core-values')">Core Values</a>
        <a @click.prevent="scrollToSection('team')">Team</a>
        <a @click.prevent="scrollToSection('testimonials')">Testimonials</a>
        <a @click.prevent="scrollToSection('faq')">FAQ</a>
        
        <div v-if="showMenu" class="mobile-actions">
          <Button text="Shop" color="#fff" bg="transparent" />
          <Button text="Contact Us" color="#014751" bg="white" />
        </div>
      </div>

      <!-- Action Buttons (visible on desktop only) -->
      <div v-if="!showMenu" class="actions">
        <Button text="Shop" color="#fff" bg="transparent" />
        <Button text="Contact Us" color="#014751" bg="white" />
      </div>

      <!-- Hamburger Icon with dynamic class binding -->
      <div :class="{ hamburger: true, 'hamburger-active': showMenu }" 
           @click="toggleMenu" 
           aria-label="Toggle Menu" 
           @animationend="resetAnimation"></div>
    </Container>
  </nav>
</template>

<script setup>
import Button from "@/components/Button/Button.vue"
import Container from "@/components/Container/Container.vue"
import { ref, onMounted, onUnmounted } from "vue"

const isScrolled = ref(false)
const showMenu = ref(false)

const toggleMenu = () => {
  showMenu.value = !showMenu.value
}

const scrollHandler = () => {
  isScrolled.value = window.scrollY > 0
}

const resetAnimation = () => {
  if (!showMenu.value) {
    showMenu.value = false;  // Reset the showMenu state to ensure it doesn't stay open
  }
}

onMounted(() => {
  window.addEventListener("scroll", scrollHandler)
})

onUnmounted(() => {
  window.removeEventListener("scroll", scrollHandler)
})

const scrollToSection = (id) => {
  const section = document.getElementById(id);
  const navbarHeight = document.querySelector('nav').offsetHeight;

  if (section) {
    const offsetTop = section.offsetTop - navbarHeight;
    window.scrollTo({
      top: offsetTop,
      behavior: 'smooth',
    });
  }
};
</script>

<style scoped>
:root {
  --hamburger-space: -6px; 
}

nav {
  width: 100%;
  background: #083F3D;
  position: sticky;
  top: 0;
  z-index: 1000;
  transition: 0.3s ease;
  backdrop-filter: blur(24px);
}

nav.scrolled {
  background: rgba(8, 63, 61, 0.7);
}

.container {
  display: flex;
  height: var(--navbar-height);
  align-items: center;
  justify-content: space-between;
}

.scrolled .container {
  height: 3.5rem;
}

img {
  width: 100%;
  height: 100%;
  object-fit: cover;
}

a {
  text-decoration: none;
  color: white;
  font-size: 16px;
  position: relative;
}

.logo {
  /* width: 10%; */
  width: 120px;
}

.link {
  width: 42%;
  display: flex;
  justify-content: space-between;
  gap: 5px;
}

.link a::before,
.link a::after {
  content: ''; 
  position: absolute; 
  bottom: 0;
  left: 0;
  width: 0;
  height: 2px;
  background-color: #fff;
  transition: 0.3s ease;
}

.link a:hover::after { 
  width: 100%;
}

.actions {
  display: flex;
  gap: 1rem;
}

/* Add rotation animation */
@keyframes rotate360 {
  0% {
    transform: rotate(0deg);
  }
  100% {
    transform: rotate(360deg);
  }
}

/* Hamburger Icon */
.hamburger {
  display: none;
  width: 20px;
  height: 2px;
  background: #fff;
  position: relative;
  cursor: pointer;
}

.hamburger::before,
.hamburger::after {
  content: "";
  position: absolute;
  background-color: #fff;
  width: 20px;
  height: 2px;
  transition: 0.3s ease;
}

.hamburger::before {
  top: -6px;
}

.hamburger::after {
  bottom: -6px;
}

/* Active Hamburger Icon (when showMenu is true) */
.hamburger-active {
  background: transparent;
  animation: rotate360 0.3s forwards;
}

.hamburger-active::before {
  top: 0;
  transform: rotate(45deg);
}

.hamburger-active::after {
  bottom: 0;
  transform: rotate(-45deg);
}

/* Dropdown Menu for Mobile */
.dropdown-menu {
  display: none;
  flex-direction: column;
  gap: 1rem;
}

.mobile-actions {
  display: flex;
  flex-direction: column;
  gap: 1rem;
  margin-top: 1rem;
}

@media (max-width: 1023px) {
    .logo {
        width: 100px;
    }

  .link, .actions {
    display: none;
  }

  .hamburger {
    display: block;
  }

  /* Show dropdown if menu is toggled */
  .dropdown-menu {
    display: flex;
    position: absolute;
    top: 100%;
    left: 0;
    right: 0;
    background-color: rgba(8, 63, 61, 0.9);
    padding: 1rem;
  }
}


@media (max-width: 767px){
    .logo {
        width: 90px;
    }
}

</style>
