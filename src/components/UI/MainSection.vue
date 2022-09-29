<template>
  <section>
    <slot></slot>
  </section>
</template>

<style scoped>
section {
  width: 100%;
  min-height: 100vh;
  padding: 1rem;
  padding-top: calc(var(--nav-height) + 1rem);
}
</style>