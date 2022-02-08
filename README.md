# david-kavenga.github.io

This website documents my learning progress in web development as part of the DevAcademy curriculum.

I hope to provide a detailed run-down of website features and style choices as well as notes for implementation.

## Contents
- [Blog pages](#Blog-pages)
  * [Identity and Values](#identity-and-values)
  * [Learning Plan](#learning-plan)
  * [Technical Blog](#technical-blog)
- [Respect the Tech](#respect-the-tech)
  * [Hello Penguin](#im-taking-this-penguin)
- [Site Planning](#site-planning)

<br>

---
## Blog pages
---
### Identity and values
### Learning Plan
### Technical Blog

<br>

---
## Respect the Tech
Here we explore tricks used to create certain elements of the site.

---

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

<br>

---
## Site Planning
A website doesn't just appear spontaneously. Some key questions needed answering.

---
### What is my site's primary purpose?
To provide an environment for exploring learning concepts from the DevAcademy course. To provide proof of my abilities, but also my progress. In other words, the site's purpose is to be a snapshot of my journey.

### Who is my audience? (is it kids, adults, academics)?
My peers and facilitators at DevAcademy, but also all users of GitHub. Because the site represents my work, I want anyone potentially interested in my work to be the target audience.

### How will I build my site to support their user experience?
I will use what I've learnt about accessibility, semantic structure, and responsive design to create a site that is maximally compatible for all users. The experience difference should be seamless between mobile and desktop as well as between sighted users and those with disability.

Letting more jarring aspects of the site (experiments or fun things) sit in their own separate space will allow for a smoother experience.

### Wireframe - can I draw my site layout on paper? Draw it!

Two separate layouts for desktop/mobile devices

<p align="center"><b>Mobile use flow</b><br>
<img src="./resources/readme/Blog Mobile.png" width="100%"></p>

The objective is to keep the navigation bar tucked in the hamburger menu at the top left of the screen. The Banner and hamburger menu will float with the rest of the page (unlike desktop version).

<p align="center"><b>Desktop Home</b><br>
<img src="./resources/readme/Blog Home.png" width="100%"></p>

Use of the site is intended to be as simple and as intuitive as possible. For navigation, a click on 'Home' or 'About' takes the user directly to those pages. Hovering on any of the nav bar buttons changes the colour and displays the dropdown, if any.

<p align="center"><b>Desktop Blog X Example</b><br>
<img src="./resources/readme/Blog Page.png" width="100%"></p>

The current page remains highlighted with the hover colour. This image doesn't show it, but the banner will adjust it's title based on the page the user is on.

### What other directories do I need (e.g images)? Where do I put that directory?
As the whole site will be created with blog posts in mind, I will need to make use of a blog directory to keep track of the individual pages. Blog posts sometimes need images, so they will be stored in something like `blog/images`. If using images becomes a regular occurrence, it might be good to further divide the images into specific blog page directories.

For the home page, I'd like to keep the structure similar. All necessary linked files can sit in their own directory `./resources`.

### Do I want the style to be applied to your blog entries also?
I think it is fine for the homepage to depart from the rest of the website, but some elements should remain consistent for ease of use. The Navigation bar, for example will be on all pages, in full or reduced form depending on the user device. I'd like for the background color/pattern to stay consistent as well as text color/link style. No scrolling for the home page if possible. It just needs to be a simple, clean representation of the site, with handy links.