<script setup>

</script>

<template>
  <section class="welcome" id="welcome">
    <div class="content">
      <h1>&lt;HelloWorld /&gt;</h1>
      <p>
        <span class="first-row">
          Hi! Welcome to my personal webpage 👋. </span>Here you'll be able to know <b>Raul, the web developer</b>: what
        are my skills and the projects I've been into. And also
        <b>Raul, the human</b>: what are my hobbies, passions and interests.
      </p>
    </div>
  </section>
</template>

<style scoped>
.welcome {
  height: 100vh;
  padding: 1em 3rem;
  padding-top: 6rem;
  background: url("Welcome.jpg");
  background-size: cover;
  background-position: center;
  background-repeat: no-repeat;
  display: flex;
  align-items: center;
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
  width: fit-content;
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