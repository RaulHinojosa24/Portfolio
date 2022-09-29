<script setup>
import MainSection from './UI/MainSection.vue';
</script>

<template>
  <MainSection id="about-me" class="about-me">
    <div class="content">
      <h2 class="title">About me</h2>
      <div class="text">
        <p>
          Hello! My name is Raul and I enjoy creating things that challenge me to think hard and learn new things. My
          interest in web development started a few years ago, when I discovered that Chrome had something called
          "developer tools"... I was like WHAT IS THAT?!, so like any curious person, I dove in and well, it got me for
          good.
        </p>
        <p>
          I'm quietly confident, resolutive, naturally curious and I will always try to help the rest of the team as
          much as I can.
        </p>
        <p>
          I love being in the nature, I like to do any kind of sport (especially volleyball and rock climbing). I
          also enjoy puzzles, playing
          chess. Train body and mind basically.
        </p>
      </div>
    </div>
    <div class="image">
      {image}
    </div>
  </MainSection>
</template>

<style scoped>
.about-me {
  display: flex;
  flex-direction: row;
  justify-content: center;
  width: 80%;
}

.content {
  width: 100%;
  display: flex;
  flex-direction: column;
  justify-content: center;
  gap: 2rem;
}

.image {
  width: 70%;
}
</style>