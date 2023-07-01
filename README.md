# Frontend Mentor - [Profile card component component.](https://www.frontendmentor.io/challenges/profile-card-component-cfArpWshJ)

## Table of contents

- [Overview](#overview)
  - [The challenge](#the-challenge)
  - [Screenshot](#screenshot)
  - [Links](#links)
- [My process](#my-process)
  - [Built with](#built-with)
  - [What I learned](#what-i-learned)

## Overview

### The challenge

Build out the project to the designs provided

### Screenshot

<details>

<summary>Click to open</summary>

![](https://i.imgur.com/koktu2e.png)

</details>

### Links

- Live Site URL: [Live](https://solracss.github.io/FrontendMentor-profile-card/)

## My process

### Built with

<div >
	<img width="30" src="https://user-images.githubusercontent.com/25181517/192108891-d86b6220-e232-423a-bf5f-90903e6887c3.png" alt="Visual Studio Code" title="Visual Studio Code"/>
	<img width="30" src="https://user-images.githubusercontent.com/25181517/192158954-f88b5814-d510-4564-b285-dff7d6400dad.png" alt="HTML" title="HTML"/>
	<img width="30" src="https://user-images.githubusercontent.com/25181517/192158956-48192682-23d5-4bfc-9dfb-6511ade346bc.png" alt="Sass" title="Sass"/>
	<img width="30" src="https://user-images.githubusercontent.com/25181517/183898674-75a4a1b1-f960-4ea9-abcb-637170a00a75.png" alt="CSS" title="CSS"/>
</div>

### What I learned

1. Working with pseudo elements `::before` `::after` to add `svg` to background.
   Alternate way of positioning top and bottom bubbles, fix it to the center of view port.

```css
.background::before,
.background::after {
	content: "";
	position: absolute;
	transform: translate(-50%, -50%);
}

.background::before {
	top: 0;
	left: 0;
	width: 100vw;
	height: 100vh;
	background: url("../img/bg-pattern-top.svg") no-repeat bottom right;
}

.background::after {
	top: 100%;
	left: 100%;
	width: 100vw;
	height: 100vh;
	background: url("../img/bg-pattern-bottom.svg") no-repeat top left;
	transform: translate(-50%, -50%);
}
```

2. Hide overflowing elements when they produce scroll bar at the bottom of screen.

```css
body {
	overflow: hidden;
}
html {
	overflow: auto;
}
```

learned from [this site.](https://stackoverflow.com/questions/41506456/why-body-overflow-not-working)
