<script setup>
import MainSection from './UI/MainSection.vue';
import AboutMe from "/AboutMe.jpg"
</script>

<template>
  <MainSection id="about-me" class="about-me">
    <div class="content">
      <div class="text">
        <h2 class="title">About me</h2>
        <div class="description">
          <p>
            Hello! My name is Raul and I enjoy creating things that challenge me to think hard and learn new things. My
            interest in web development started a few years ago, when I discovered that Chrome had something called
            "developer tools"... I was like WHAT IS THAT?!, so like any curious person, I dove in and well, it got me
            for
            good.
          </p>
          <p>
            I'm quietly confident, resolutive, naturally curious and I will always try to help the rest of the team as
            much as I can.
          </p>
          <p>
            I love being in the nature, I like to do any kind of sport (especially volleyball and climbing). I
            also enjoy puzzles, playing
            chess.
          </p>
          <p>Exercicing mind and body is the best!</p>
        </div>
      </div>
      <div class="image">
        <img :src="AboutMe" alt="">
      </div>
    </div>
  </MainSection>
</template>

<style scoped>
.about-me {
  display: flex;
  justify-content: center;
  align-items: center;
}

.content {
  display: flex;
  flex-direction: row;
  justify-content: center;
  align-items: center;
  display: grid;
  grid-template-columns: 3fr 2fr;
  width: 90%;
}

.text {
  display: flex;
  flex-direction: column;
  justify-content: center;
  gap: 2rem;
  padding: 2rem;
}

.title {
  text-transform: capitalize;
  font-size: 1.8rem;
  width: 70%;
  border-bottom: 2px solid var(--blue);
}

.title::before {
  content: "";
  width: 2ch;
  display: inline-block;
}

.description {
  display: flex;
  flex-direction: column;
  gap: 1rem;
}

.image {
  display: flex;
  justify-content: center;
  margin: 1rem;
  position: relative;
}

.image img {
  object-fit: cover;
  width: 100%;
}

.image::after {
  content: "";
  position: absolute;
  top: .5rem;
  left: .5rem;
  z-index: -10;
  border: 2px solid rgb(0, 0, 0, .5);
  width: 100%;
  height: 100%;
}
</style>