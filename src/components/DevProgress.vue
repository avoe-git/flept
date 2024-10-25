<template>
    <section>
        <div class="devprog">
                <br>
                <ol class="progress-bar">
                    <li v-for="(step, index) in steps" :key="index"
                        :class="{'is-complete': step.isComplete, 'is-hovered': step.isHovered, 'has-changes': step.hasChanges}"
                        @mouseover="hoverStep(index)"
                        @mouseleave="hoverStep(null)">
                    <span>{{ step.label }}</span>
                    </li>
                </ol>
        </div>
    </section>
  </template>
  
  <script>
  export default {
    data() {
      return {
        steps: [
          { label: "Ideas & Design", isComplete: true, isHovered: false },
          { label: "NPM Build", isComplete: true, isHovered: false },
          { label: "Hosting on Vercel", isComplete: true, isHovered: false},
          { label: "Private Beta", isComplete: true, isHovered: true ,isActive:true, hasChanges: true},
          { label: "Public Beta", isComplete: false, isHovered: false },
          { label: "PreRelease", isComplete: false, isHovered: false },
          { label: "First Official Release", isComplete: false, isHovered: false },
          { label: "v.2.0.0", isComplete: false, isHovered: false },
          { label: "Open to User Requests", isComplete: false, isHovered: false },
          { label: "Latest Stable Version", isComplete: false, isHovered: false }
        ]
      };
    },
    methods: {
      hoverStep(index) {
        this.steps.forEach((step, idx) => {
          step.isHovered = index === idx;
        });
      }
    }
  };
  </script>
  
  <style>
    .devprog {
        font-family: Outfit, sans-serif;
        font-weight: 600;
        text-align: center;
        margin: 20px;
        /* background-color: #d3d3d3;  Lighter background color */
        padding: 20px 30px 40px 30px;
        border-radius: 10px;
        /* box-shadow: 0 0 10px rgba(0, 0, 0, 0.3); */
        box-shadow: 
            0 0 5px #000000,     /* Inner glow */
            0 0 10px #000000,    /* Medium glow */
            0 0 20px #000000,    /* Larger glow */
            0 0 30px #000000,    /* Outer glow */
            0 0 40px #000000;    /* More intense glow */
            /*0 0 50px #ffffff;     Strongest glow */
        }
    :root {
        --color-white: #fff;
        --color-black: #333;
        --color-gray: #75787b;
        --color-gray-light: #bbb;
        --color-gray-disabled: #e8e8e8;
        --color-green: #53a318;
        --color-green-dark: #383;
        --font-size-small: .75rem;
        --font-size-default: .875rem;
    }
    
    * {
        box-sizing: border-box;
    }
    
    body {
        margin: 2rem;
        font-family: 'Open Sans', sans-serif;
        color: var(--color-black);
    }
    
    h2 {
        color: var(--color-green);
        font-size: var(--font-size-small);
        line-height: 1.5;
        font-weight: 400;
        text-transform: uppercase;
        letter-spacing: 3px;
    }
    
    section {
        margin-bottom: 2rem;
    }
    
    .progress-bar {
        display: flex;
        justify-content: space-between;
        list-style: none;
        padding: 0;
        margin: 0 0 1rem 0;
    }
    
    .progress-bar li {
        flex: 2;
        position: relative;
        padding: 0 0 14px 0;
        font-size: var(--font-size-default);
        line-height: 1.5;
        color: var(--color-green);
        font-weight: 600;
        white-space: nowrap;
        overflow: visible;
        min-width: 0;
        text-align: center;
        border-bottom: 2px solid var(--color-gray-disabled);
    }
    
    .progress-bar li:first-child,
    .progress-bar li:last-child {
        flex: 1;
    }
    
    .progress-bar li:last-child {
        text-align: right;
    }
    
    .progress-bar li:before {
        content: "";
        display: block;
        width: 8px;
        height: 8px;
        background-color: var(--color-gray-disabled);
        border-radius: 50%;
        border: 2px solid var(--color-white);
        position: absolute;
        left: calc(50% - 6px);
        bottom: -7px;
        z-index: 3;
        transition: all .2s ease-in-out;
    }
    
    .progress-bar li:first-child:before {
        left: 0;
    }
    
    .progress-bar li:last-child:before {
        right: 0;
        left: auto;
    }
    
    .progress-bar span {
        transition: opacity .3s ease-in-out;
    }
    
    .progress-bar li:not(.is-active) span {
        opacity: 0;
    }
    
    .progress-bar .is-complete:not(:first-child):after,
    .progress-bar .is-active:not(:first-child):after {
        content: "";
        display: block;
        width: 100%;
        position: absolute;
        bottom: -2px;
        left: -50%;
        z-index: 2;
        border-bottom: 2px solid var(--color-green);
    }
    
    .progress-bar li:last-child span {
        width: 200%;
        display: inline-block;
        position: absolute;
        left: -100%;
    }
    
    .progress-bar .is-complete:last-child:after,
    .progress-bar .is-active:last-child:after {
        width: 200%;
        left: -100%;
    }
    
    .progress-bar .is-complete:before {
        background-color: var(--color-green);
    }
    
    .progress-bar .is-active:before,
    .progress-bar li:hover:before,
    .progress-bar .is-hovered:before {
        background-color: var(--color-white);
        border-color: var(--color-green);
    }
    
    .progress-bar li:hover:before,
    .progress-bar .is-hovered:before {
        transform: scale(1.33);
    }
    
    .progress-bar li:hover span,
    .progress-bar li.is-hovered span {
        opacity: 1;
    }
    
    .progress-bar:hover li:not(:hover) span {
        opacity: 0;
    }
    
    .progress-bar li:is-active, is-hovered span {
        opacity: 1 !important;
    }
    .progress-bar .has-changes {
        opacity: 1 !important;
    }
    
    .progress-bar .has-changes:before {
        content: "";
        display: block;
        width: 8px;
        height: 8px;
        position: absolute;
        left: calc(50% - 4px);
        bottom: -20px;
        background-image: url('data:image/svg+xml;charset=utf-8,%3Csvg%20xmlns%3D%22http%3A%2F%2Fwww.w3.org%2F2000%2Fsvg%22%20viewBox%3D%220%200%208%208%22%3E%3Cpath%20fill%3D%22%23ed1c24%22%20d%3D%22M4%200l4%208H0z%22%2F%3E%3C%2Fsvg%3E');
    }
  </style>
  