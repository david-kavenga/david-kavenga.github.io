# david-kavenga.github.io

This website documents my learning progress in web development as part of the DevAcademy curriculum.

I hope to provide a detailed run-down of website features and style choices as well as notes for implementation.

## Contents
- [Blog pages](#Blog-pages)
- [Respect the Tech](#respect-the-tech)
  * [Hello Penguin](#im-taking-this-penguin)

---
## Blog pages
---

## Respect the Tech
Here we explore tricks used to create certain elements of the site.


### I'm taking this penguin

A waving penguin used in part of the Responsive Web Development CSS intro course from freecodecamp.org.
It is displayed on the index page using a small `<iframe>` with no border. The penguin itself is made using CSS and HTML, using CSS variables to provide an easy way to change colors.

```CSS
.right-hand {
    top: 5%;
    left: 25%;
    background: var(--penguin-skin, black);
    width: 30%;
    height: 60%;
    border-radius: 30% 30% 120% 30%;
    transform: rotate(130deg);
    z-index: -1;
    animation-duration: 3s;
    animation-name: wave;
    animation-iteration-count: infinite;
    transform-origin:0% 0%;
    animation-timing-function: linear;
  }

  @keyframes wave {
      10% {
        transform: rotate(110deg);
      }
      20% {
        transform: rotate(130deg);
      }
      30% {
        transform: rotate(110deg);
      }
      40% {
        transform: rotate(130deg);
      }
    }
```
This shows some of the key rules which dictate the movement of the penguin's right hand. Animation duration, name, iteration count, transformation origin and timing function are defined. `@keyframes` defines rules for the animation. In this case, the arm is rotated four times during the animation. The percentages correspond to how far through the animation (of the total 3s) the transformation occurs.