<script setup>
import { ref, onMounted } from 'vue';

const darkTheme = ref("dark");

const getThemeLocalStorage = () => {
  return localStorage.getItem("dark-theme");
}

const updateTheme = (darkThemeUpdated) => {
  darkTheme.value = darkThemeUpdated;
  localStorage.setItem("dark-theme", darkTheme.value);
  darkTheme.value ? document.body.classList.add("dark") : document.body.classList.remove("dark")
}

const toggleTheme = () => {
  const newTheme = darkTheme.value ? "" : "dark";
  updateTheme(newTheme);
}

const getMediaPreference = () => {
  const hasDarkPreference = window.matchMedia(
    "(prefers-color-scheme: dark)"
  ).matches;

  if (hasDarkPreference) {
    return "dark";
  } else {
    return "";
  }
}

onMounted(() => {
  const initialDarkTheme = getThemeLocalStorage() ?? getMediaPreference();
  updateTheme(initialDarkTheme);
})

</script>

<template>
  <input @change="toggleTheme" id="checkbox" type="checkbox" class="switch-checkbox" />
  <label for="checkbox" class="switch-label">
    <span>🌙</span>
    <span>☀️</span>
    <div class="switch-toggle" :class="{ 'switch-toggle-checked': darkTheme }"></div>
  </label>
</template>

<style scoped>
.switch-checkbox {
  display: none;
}

.switch-label {
  width: var(--toggle-size);
  height: calc(var(--toggle-size) * 0.5);
  border-radius: var(--toggle-size);
  border: calc(var(--toggle-size) * 0.025) solid var(--accent-color);
  font-size: calc(var(--toggle-size) * 0.3);

  align-items: center;
  background-color: var(--toggle-bg-color);
  cursor: pointer;
  display: flex;
  position: relative;
  transition: background-color 0.5s ease;
  justify-content: space-between;
  z-index: 1;
}

.switch-toggle {
  position: absolute;
  background-color: var(--toggler-color);
  border-radius: 50%;
  top: calc(var(--toggle-size) * 0.025);
  left: calc(var(--toggle-size) * 0.025);
  height: calc(var(--toggle-size) * 0.4);
  width: calc(var(--toggle-size) * 0.4);
  transform: translateX(0);
  transition: transform 0.3s ease, background-color 0.5s ease;
}

.switch-toggle-checked {
  transform: translateX(calc(var(--toggle-size) * 0.5)) !important;
}
</style>