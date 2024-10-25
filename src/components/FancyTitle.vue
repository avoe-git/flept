<template>
    <h2 class="fancy" :style="styleVars">
      <slot></slot>
    </h2>
  </template>
  
  <script>
  export default {
    name: 'FancyTitle',
    props: {
      width: {
        type: String,
        default: '50vw',
      },
      color: {
        type: String,
        default: '#C44D58',
      },
      borderThickness: {
        type: String,
        default: '4px',
      },
      gap: {
        type: String,
        default: '40px',
      },
    },
    computed: {
      styleVars() {
        return {
          '--w': this.width,
          '--c': this.color,
          '--b': this.borderThickness,
          '--g': this.gap,
        };
      },
    },
  };
  </script>
  
  <style scoped>
    .fancy {
    --b: 6px; /* control the border thickness */
    --w: 80px; /* control the width of the line*/
    --g: 15px; /* control the gap */
    --c: #0B486B;
  
    width: fit-content;
    font-family: Outfit, sans-serif;
    font-weight: 400;
    padding: 0 1em;
    line-height: 1.6em;
    border: 1px solid;
    color: #fff;
    background: 
      conic-gradient(from 45deg at left, var(--c) 25%, #0000 0) 0,
      conic-gradient(from -135deg at right, var(--c) 25%, #0000 0) 100%;
    background-size: 51% 100%;
    background-origin: border-box;
    background-repeat: no-repeat;
    border-image: 
      linear-gradient(
        #0000 calc(50% - var(--b)/2),
        var(--c) 0 calc(50% + var(--b)/2),
        #0000 0
      )
      1/0 var(--w)/calc(var(--w) + var(--g));
    margin-inline: auto;
  }
  </style>
  