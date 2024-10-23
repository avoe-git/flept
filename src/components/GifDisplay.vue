<template>
  <div class="gif-container">
    <img :src="gifUrl" alt="Looping GIF" class="gif" />
    <p class="gif-text">{{ text }}</p>
    
    <!-- Buttons Section -->
    <div class="button-container">
      <button @click="openGitHub" class="btn">Project on GitHub</button>
      <button @click="contactDeveloper" class="btn">Contact Developer</button>
    </div>
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
  methods: {
    openGitHub() {
      window.open('https://github.com/avoe-git/flept', '_blank');
    },
    contactDeveloper() {
      window.location.href = 'mailto:inuser027+flept@gmail.com';
    },
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
  box-shadow: 0 0 10px rgba(0, 0, 0, 0.3);
}

.gif {
  width: 100px; /* Adjust the width */
  height: 100px; /* Adjust the height */
}

.gif-text {
  font-size: 1.5em;
  margin-top: 10px;
  color: #333;
}

/* Button styles */
.button-container {
  margin-top: 15px;
}

.btn {
  background-color: #e3ebe3; /* Green button */
  color: rgb(12, 12, 12);
  border: none;
  padding: 10px 15px;
  font-size: 1em;
  cursor: pointer;
  margin: 5px;
  border-radius: 5px;
  transition: background-color 0.3s;
}

.btn:hover {
  background-color: #45a049; /* Slightly darker green on hover */
}
</style>
