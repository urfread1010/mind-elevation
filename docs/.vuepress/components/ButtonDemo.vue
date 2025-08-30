<template>
  <div class="demo-wrapper">
    <button class="demo-btn" @click="showMessage">
      点我一下
    </button>
  </div>
</template>

<script setup>
function showMessage() {
  alert("🎉 恭喜，你点到我啦！");
}
</script>

<style scoped>
.demo-wrapper {
  margin: 1rem 0;
}

.demo-btn {
  background: #42b983; /* VuePress 绿色 */
  color: white;
  padding: 0.6rem 1.2rem;
  border-radius: 6px;
  border: none;
  cursor: pointer;
  font-size: 16px;
  transition: background 0.2s ease;
}

.demo-btn:hover {
  background: #369a6e;
}
</style>
