<template>
  <div class="wrapper" :style="{ backgroundColor: backgroundColor }">
    <button @click="changeColor">Change Background</button>
  </div>
</template>

<script>
export default {
  data() {
    return {
      backgroundColor: 'white',
    };
  },
  methods: {
    changeColor() {
      const colors = ['#FF6B6B', '#4ECDC4', '#FFD93D', '#6A4C93', '#1A535C'];
      this.backgroundColor = colors[Math.floor(Math.random() * colors.length)];
    },
  },
};
</script>

<style scoped>
.wrapper {
  height: 100vh;
  display: flex;
  justify-content: center;
  align-items: center;
  transition: background-color 0.5s;
}

button {
  padding: 1rem 2rem;
  font-size: 1.2rem;
  font-weight: bold;
  border: none;
  border-radius: 8px;
  background-color: #333;
  color: white;
  cursor: pointer;
}
</style>



