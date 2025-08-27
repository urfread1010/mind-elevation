<script setup>
const items = [1, 2, 3, 4, 5]
</script>

<template>
  <nav class="right-floating-nav">
    <button v-for="item in items" :key="item" class="nav-btn">
      {{ item }}
    </button>
  </nav>
</template>

<style scoped>
.right-floating-nav {
  position: fixed;
  top: 50%;
  right: 10px;
  transform: translateY(-50%);
  background: rgba(255, 255, 255, 0.9);
  padding: 1rem;
  border-radius: 8px;
  box-shadow: 0 0 8px rgba(0,0,0,0.15);
  display: flex;
  flex-direction: column;
  gap: 1rem;
  z-index: 9999;
}

.nav-btn {
  background-color: #42b983;
  border: none;
  color: white;
  padding: 0.5rem 1rem;
  border-radius: 4px;
  cursor: pointer;
}
</style>
