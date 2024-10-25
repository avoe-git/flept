<template>
  <div id="app">
    <Sphere></Sphere>
    <GifDisplay />
    <div>
    <FancyTitle :width="'50vw'" :color="'#100c0c'" :border-thickness="'4px'" :gap="'20px'">
      Developmnent Progress
    </FancyTitle>
    </div>
    <ProgressBar />
  </div>
</template>

<script>
import GifDisplay from './components/GifDisplay.vue';
import ProgressBar from './components/DevProgress.vue';
import FancyTitle from './components/FancyTitle.vue';
import Sphere from './components/Sphere.vue';

export default {
  components: {
    GifDisplay,
    ProgressBar,
    FancyTitle,
    Sphere
  },
};
</script>

<style>
@import url('https://fonts.googleapis.com/css2?family=Outfit:wght@100..900&display=swap');
/* Global styles for the entire app */
body {
  margin: 0;
  padding: 0;
  background-color: #1e1e1e; /* Change this color to what you want */
  font-family: 'Arial, sans-serif';
}

#app {
  /* display: flex; */
  justify-content: center;
  align-items: center;
  height: 100vh; /* Full viewport height */
}
</style>
