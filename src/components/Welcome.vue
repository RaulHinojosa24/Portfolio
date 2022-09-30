<script setup>
import MainSection from './UI/MainSection.vue';
</script>

<template>
  <MainSection class="welcome" id="welcome">
    <p class="sentence">Hi,</p>
    <p class="sentence">I'm Raul,</p>
    <p class="sentence">web developer.</p>
  </MainSection>
</template>

<style scoped>
.welcome {
  height: 100vh;
  padding-left: 3rem;
  padding-right: 3rem;
  background: url("Welcome.jpg");
  background-size: cover;
  background-position: right;
  background-repeat: no-repeat;
  display: flex;
  flex-direction: column;
  justify-content: center;
  align-items: flex-start;
  gap: 2rem;
}

.sentence {
  font-size: clamp(1rem, 8vw, 5rem);
  font-weight: bold;
  padding: .5rem 1rem;

  background-color: var(--primary-color);
  color: var(--secondary-color);
  box-shadow: var(--card-box-shadow);
  transition: box-shadow var(--theme-transition-duration);
}

.sentence:last-of-type {
  color: var(--accent-color);
}

.sentence:last-of-type::after {
  content: "|";
  font-weight: 300;
  color: black;
  animation: type-blink 1s steps(1) infinite;
}

@keyframes type-blink {
  50% {
    color: transparent;
  }
}
</style>