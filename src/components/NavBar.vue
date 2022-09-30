<script setup>
import Logo from "/logo.svg"
import ThemeToggler from "./ThemeToggler.vue";
</script>

<template>
  <nav class="nav-bar">
    <ul>
      <!-- <div class="left-side"> -->
      <li class="nav-logo">
        <a href="#">
          <img :src="Logo" alt="" class="logo">
        </a>
      </li>
      <!-- <div class="name-developer">
          <span class="name">Raul Hinojosa Perez</span>
          <span class="developer">Full Stack Web Developer</span>
        </div> -->
      <!-- </div> -->
      <!-- <ThemeToggler /> -->
      <!-- <li class="nav-item"><a href="#welcome">Welcome</a></li> -->
      <li class="nav-item"><a href="#about-me">About Me</a></li>
      <li class="nav-item"><a href="#skills">Skills</a></li>
      <li class="nav-item"><a href="#">Portfolio</a></li>
      <li class="nav-item"><a href="#">Contact</a></li>
    </ul>
  </nav>
</template>

<style scoped>
.nav-bar {
  width: 100%;
  position: fixed;
  top: 0;
  left: 0;
  background-color: rgba(255, 255, 255, .9);
  backdrop-filter: blur(20px);
  box-shadow: var(--box-shadow);
  z-index: 100;
  height: var(--nav-height);
}

.nav-bar ul {
  height: 100%;
  margin: 0;
  padding: 0 5%;
  display: flex;
  list-style: none;
  align-items: center;
  justify-content: center;
  gap: 1vw;
}

.nav-item a {
  color: var(--accent-color);
  transition: box-shadow 0.3s, color 0.3s;
  padding: 0.5rem 1rem;
  font-weight: 600;
}

.nav-item a:hover {
  box-shadow: inset 0 -50px 0 0 var(--accent-color);
  color: white;
}

.logo {
  aspect-ratio: 1;
  width: 2rem;
}
</style>
