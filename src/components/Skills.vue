<script setup>
import MainSection from './UI/MainSection.vue';
import Bootstrapsvg from "../assets/svg-components/Bootstrap.vue"
import CSSsvg from "../assets/svg-components/CSS.vue"
import HTMLsvg from "../assets/svg-components/HTML.vue"
import Javasvg from "../assets/svg-components/Java.vue"
import Javascriptsvg from "../assets/svg-components/Javascript.vue"
import MongoDBsvg from "../assets/svg-components/MongoDB.vue"
import MySQLsvg from "../assets/svg-components/MySQL.vue"
import Reactsvg from "../assets/svg-components/React.vue"
import Springsvg from "../assets/svg-components/Spring.vue"
import Vuesvg from "../assets/svg-components/Vue.vue"
import Nodejssvg from '../assets/svg-components/Nodejs.vue';
import Angularsvg from '../assets/svg-components/Angular.vue';
import Phpsvg from '../assets/svg-components/Php.vue';
import Pythonsvg from '../assets/svg-components/Python.vue';
</script>

<template>
  <MainSection id="skills" class="skills">
    <div class="content">
      <div class="languages">
        <h2 class="title">Skills</h2>
        <div>
          <p>These are the programming languages and skills sorted from most to least proficient:</p>
          <div>
            <h3 class="sub-title">High</h3>
            <p class="languages-listed">
              <CSSsvg />
              <HTMLsvg />
              <Javascriptsvg />
              <Reactsvg />
              <Vuesvg />
            </p>
            <h3 class="sub-title">Medium</h3>
            <p class="languages-listed">
              <Javasvg />
              <MySQLsvg />
              <Springsvg />
            </p>
            <h3 class="sub-title">Basic</h3>
            <p class="languages-listed">
              <Bootstrapsvg />
              <MongoDBsvg />
            </p>
            <h3 class="sub-title">Wishlist</h3>
            <p class="languages-listed">
              <Nodejssvg />
              <Angularsvg />
              <Phpsvg />
              <Pythonsvg />
            </p>
          </div>
        </div>
      </div>
      <div class="experience">
        <h2 class="title">Experience</h2>
        <div class="description">
          <p>
            In the years, I’ve cultivated my passion for coding by studying a higher degree training course about web
            development and recently a full stack developer bootcamp.
            Thanks to that and to self-learning, nowadays I'm able to build apps like this and more.
          </p>
          <p>
            I have full stack experience and knowledge, but right now I'm specializing in front end, more specifically
            in ReactJS. It is a library with a lot of job opportunities and I see it as a good chance to start my
            professional career as a developer.
          </p>
        </div>
      </div>
    </div>
  </MainSection>
</template>

<style scoped>
.skills {
  display: flex;
  justify-content: center;
  align-items: center;
}

.icon {
  width: 50px;
}

.content {
  display: flex;
  flex-direction: row;
  justify-content: center;
  align-items: center;
  gap: 1rem;
  width: 90%;
}

.experience,
.languages {
  display: flex;
  flex-direction: column;
  justify-content: center;
  gap: 2rem;
  width: 100%;
}

.sub-title {
  margin: 1rem 0 .5rem 0;
}

.languages-listed {
  display: flex;
  flex-direction: row;
  align-items: center;
  gap: .5rem;
}

.languages-listed>* {
  width: 3rem;
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
</style>