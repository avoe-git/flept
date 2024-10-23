<template>
  <div id="app">
    <GifDisplay />
  </div>
</template>

<script>
import GifDisplay from './components/GifDisplay.vue';

export default {
  components: {
    GifDisplay,
  },
};
</script>

<style>
/* Global styles for the entire app */
body {
  margin: 0;
  padding: 0;
  background-color: #1e1e1e; /* Change this color to what you want */
  font-family: 'Arial, sans-serif';
}

#app {
  display: flex;
  justify-content: center;
  align-items: center;
  height: 100vh; /* Full viewport height */
}
</style>
