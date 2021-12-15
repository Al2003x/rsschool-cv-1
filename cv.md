# Victor Danilov

-----------------

### Contacts:
* **Discord**: Al2003x
* **Telegram**: Al2003x
* **Mail**: Danilovvik33@gmail.com
* **Github**: https://github.com/Al2003x

### Work experience:
No work experience at the moment

### Education and courses:
1. HTMLAcademy: Intensive course "Basic HTML & CSS", Profession "React-developer #1"
2. RSScholl: JSFE2021Q1
3. HTML, CSS, JS, Git video courses on YouTube channel

### Skills
* HTML
* CSS3 & SCSS
* Git
* JS
* Gulp & webpack
* Figma

### Code example:
```javascript (project: virtual-piano)
const piano = document.querySelector(".piano");
const pianoKeys = document.querySelectorAll(".piano-key");
const openFullScreen = document.querySelector(".openfullscreen");
const buttons = document.querySelectorAll(".btn");
const btnContainer = document.querySelector(".btn-container");

function playAudio(src) {
  const audio = new Audio();
  audio.src = src;
  audio.currentTime = 0;
  audio.play();
}

piano.addEventListener("mousedown", (e) => {
  if (e.target.classList.contains("piano-key")) {
    e.target.classList.add("piano-key-active", "piano-key-active-pseudo");
    e.target.classList.remove("piano-key-remove-mouse");
    let note = e.target.dataset.note;
    let src = `assets/audio/${note}.mp3`;
    playAudio(src);
  }
});

piano.addEventListener("mouseup", (e) => {
  e.target.classList.remove("piano-key-active", "piano-key-active-pseudo");
  e.target.classList.add("piano-key-remove-mouse");
});

// Fullscreen

function toggleFullScreen() {
  if (!document.fullscreenElement) {
    document.documentElement.requestFullscreen();
  } else {
    document.exitFullscreen();
  }
}

openFullScreen.addEventListener("click", () => toggleFullScreen());
```
### Language:

English in the learning process