<script setup>
import Logo from "/logo.svg"
import ThemeToggler from "./ThemeToggler.vue";
</script>

<template>
  <nav class="nav-bar">
    <ul>
      <div class="left-side">
        <li class="nav-item">
          <a href="#">
            <img :src="Logo" alt="" class="logo">
          </a>
        </li>
        <div class="name-developer">
          <span class="name">Raul Hinojosa Perez</span>
          <span class="developer">Full Stack Web Developer</span>
        </div>
      </div>
      <!-- <ThemeToggler /> -->
      <li class="nav-item"><a href="#welcome">Welcome</a></li>
      <li class="nav-item"><a href="#about-me">About Me</a></li>
      <li class="nav-item"><a href="#">Skills</a></li>
      <li class="nav-item"><a href="#">Portfolio</a></li>
    </ul>
  </nav>
</template>

<style scoped>
.nav-bar {
  width: 100%;
  position: fixed;
  top: 0;
  left: 0;
  background-color: var(--primary-color);
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
  gap: .5vw;
}

.nav-bar>ul>li a {
  color: var(--accent-color);
  transition: box-shadow 0.3s, color 0.3s;
  padding: 0.5rem 1rem;
  font-weight: 600;
}

.nav-bar>ul>li a:hover {
  box-shadow: inset 0 -50px 0 0 var(--accent-color);
  color: white;
}

.nav-bar .left-side {
  margin-right: auto;
  display: flex;
  align-items: center;
  gap: 1rem;
}

.name-developer {
  display: flex;
  flex-direction: column;
  justify-content: center;
}

.name-developer .name {
  font-size: 1.2rem;
  font-weight: bold;
}

.name-developer .developer {
  font-size: 0.8rem;
  font-weight: bold;
  color: var(--accent-color);
}

.logo {
  aspect-ratio: 1;
  width: 2rem;
}
</style>
