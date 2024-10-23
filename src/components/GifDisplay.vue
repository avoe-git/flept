<template>
  <div class="gif-container">
    <img :src="gifUrl" alt="Looping GIF" class="gif" />
    <p class="gif-text">{{ text }}</p>
  </div>
</template>

<script>
import myGif from '../assets/icons8-toolsss.gif';

export default {
  data() {
    return {
      gifUrl: myGif,
      text: 'Site is under development!',
    };
  },
};
</script>

<style scoped>
.gif-container {
  text-align: center;
  margin: 20px;
  background-color: #d3d3d3; /* Lighter background color */
  padding: 20px;
  border-radius: 10px;
  box-shadow: 0 0 10px rgba(0, 0, 0, 0.3); /* Softer shadow */
}

.gif {
  width: 100px; /* Adjust the width */
  height: 100px; /* Adjust the height */
}

.gif-text {
  font-size: 1.5em;
  margin-top: 10px;
  color: #333; /* Slightly darker text color for contrast */
}
</style>
