# Flept by avoe.dev - Development branch

## Welcome to development branch!

> [!NOTE]
> This branch was created from main

## Libraries

<div class="codepen" data-height="300" data-theme-id="dark" data-default-tab="result" data-slug-hash="MWNOjoY" data-pen-title="Progress Bar - FLEPT by avoe.dev" data-user="avoe"  data-prefill='{"title":"Progress Bar - FLEPT by avoe.dev","tags":[],"scripts":[],"stylesheets":[]}'>
  <pre data-lang="html">&lt;section>
  &lt;h2> Development Progress&lt;/h2>

  &lt;ol class="progress-bar">
    &lt;li class="is-complete">&lt;span>Ideas &amp; Design&lt;/span>&lt;/li>  
    &lt;li class="is-complete">&lt;span>NPM Build&lt;/span>&lt;/li>  
    &lt;li class="is-complete">&lt;span>Hosting on Vercel&lt;/span>&lt;/li>
    &lt;li class="is-complete is-hovered">&lt;span>Private Beta&lt;/span>&lt;/li>  
    &lt;li>&lt;span>Public Beta&lt;/span>&lt;/li>
    &lt;li>&lt;span>PreRelease&lt;/span>&lt;/li>
    &lt;li>&lt;span>First Official Release&lt;/span>&lt;/li>  
    &lt;li>&lt;span>v.2.0.0&lt;/span>&lt;/li>
    &lt;li>&lt;span>Open to User Requests&lt;/span>&lt;/li>
    &lt;li>&lt;span>Latest Stable Version&lt;/span>&lt;/li>  
  &lt;/ol>
&lt;/section></pre>
  <pre data-lang="css">:root {
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
  color: var(--color-gray);
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

.x-ray .progress-bar,
.x-ray .progress-bar li {
  border: 1px dashed red;
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
}</pre></div>
<script async src="https://cpwebassets.codepen.io/assets/embed/ei.js"></script>



<section style=":root {
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

- {
  box-sizing: border-box;
  }

body {
margin: 2rem;
font-family: 'Open Sans', sans-serif;
color: var(--color-black);
}

h2 {
color: var(--color-gray);
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

.x-ray .progress-bar,
.x-ray .progress-bar li {
border: 1px dashed red;
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

">

  <h2>Current development logs __(Git-Visual)__</h2>

  <ol class="progress-bar">
    <li class="is-complete"><span>Objective &amp; Template</span></li>  
    <li class="is-complete"><span>Options</span></li>  
    <li class="is-complete is-hovered"><span>Step</span></li>
    <li class="is-complete "><span>In a Nutshell</span></li>  
    <li class="is-complete"><span>Step</span></li>
    <li class="is-complete"><span>Step</span></li>
    <li class="is-complete"><span>Launch Date</span></li>  
    <li><span>Step</span></li>
    <li><span>Step</span></li>
    <li><span>Agreement</span></li>  
  </ol>
</section>
