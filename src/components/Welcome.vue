<script setup>
import MainSection from './UI/MainSection.vue';
</script>

<template>
  <MainSection class="welcome" id="welcome">
    <!-- <div class="content">
      <h1>&lt;HelloWorld /&gt;</h1>
      <h1>Hi, I'm Raul</h1>
      <p>
        <span class="first-row">
          Hi! Welcome to my personal webpage 👋. </span>Here you'll be able to know <b>Raul, the web developer</b>: what
        are my skills and the projects I've been into. And also
        <b>Raul, the human</b>: what are my hobbies, passions and interests.
      </p>
    </div> -->

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
  background-color: var(--primary-color);
  color: var(--secondary-color);
  font-size: clamp(1rem, 8vw, 5rem);

  box-shadow: -5px -5px var(--secondary-color);
  transition: box-shadow .5s;

  font-weight: bold;
  padding: .5rem 1rem;
}

.dark .sentence {
  box-shadow: 5px 5px var(--secondary-color);
}

.sentence:last-of-type {
  color: var(--accent-color);
}

.welcome .content {
  background-color: var(--primary-color);
  box-shadow: var(--box-shadow);
  width: 60%;
  max-height: 100%;
  padding: 3rem;
  padding-top: 4rem;
  display: flex;
  flex-direction: column;
  align-items: center;
  justify-content: center;
  text-align: center;
  position: relative;
  animation: enter-from-left 0.5s ease-out;
}

.welcome .content h1 {
  margin: 0;
  padding: 0.2rem 2rem;
  background-color: var(--secondary-color);
  color: var(--accent-color);
  font-size: 3rem;
  position: absolute;
  top: 0;
  translate: 0 -50%;
  font-family: 'Cascadia Code', Consolas, 'Courier New', monospace;
}

.welcome .content h1::after {
  content: "|";
  font-weight: 300;
  color: rgb(174, 175, 173);
  animation: type-blink 1.5s steps(1) infinite;
}

@keyframes type-blink {
  50% {
    color: transparent;
  }
}

.welcome .content p .first-row {
  display: block;
  margin-bottom: 0.2rem;
  font-size: 1.3rem;
}

@keyframes enter-from-left {
  0% {
    opacity: 0;
    transform: translateX(-3rem);
  }

  100% {
    opacity: 1;
    transform: translateX(0rem);
  }
}
</style>