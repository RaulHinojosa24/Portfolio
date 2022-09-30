<template>
  <section>
    <slot></slot>
  </section>
</template>

<style scoped>
section {
  width: 100%;
  max-width: 1600px;
  min-height: 100vh;
  padding: 1rem;
  padding-top: calc(var(--nav-height) + 1rem);
  margin: 0 auto;
}
</style>