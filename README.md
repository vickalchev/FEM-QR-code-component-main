# Frontend Mentor - QR code component

This is a solution to the [QR code component challenge on Frontend Mentor](https://www.frontendmentor.io/challenges/qr-code-component-iux_sIO_H). Frontend Mentor challenges help you improve your coding skills by building realistic projects.

## Table of contents

- [Overview](#overview)
  - [Screenshot](#screenshot)
  - [Links](#links)
- [My process](#my-process)
  - [Built with](#built-with)
  - [What I learned](#what-i-learned)
  - [Continued development](#continued-development)
  - [Useful resources](#useful-resources)
- [Author](#author)
- [Acknowledgments](#acknowledgments)

**Note: Delete this note and update the table of contents based on what sections you keep.**

## Overview

The goal of this challenge was to set up a QR code panel. The purpose of the challenge is to practice aligning various elements.

### Screenshot

![](/design/Screenshot-Solution.jpeg)

### Links

- Solution URL: [Add solution URL here](https://your-solution-url.com)
- Live Site URL: [Add live site URL here](https://your-live-site-url.com)

## My process

- I started by analyzing the structure of the panel. We have one container that holds a picture (the QR code) and two types of text - a heading and a paragraph style.
- The containers are nested, so we need to make sure they align properly and there is no overflow.
- I set up the <main class="container"> as the outermost container to hold the whole panel.
- For the setup of the QR code I had two options:
  - an image, which is resized to fit;
  - another container with an image background;
    It turned out setting up the first option was easier, so I went with that one. Also, it appears to take less lines of code - also a plus.
- After I set up the panel (relatively easy) I had to center the panel.
- I used Flexbox in <body>, so I can get the <main> centered in the middle of the window. I chose Flexbox for this solution as we are working with only two-dimentional positioning of one item (the component). So, I needed to simply justify it and align it to centre.
- Such an alignment is easy to do with Flexbox:
  ```CSS
  display: flex;
  align-items: center;
  justify-content: center;
  ```
- Just when I thought I was done, something else popped up: I had a footer that aligned to the right of my component. I wanted it under but I couldn't figure our how to do it.
- This is when I discovered that you can arrange components with Flexbox around an axis - row or column. To get things lined up vertically, I have to arrange the components around a column axis. To do this, I had to add this line of code:
  flex-direction: column;
  It appeared that be dafault my items were getting aligned by row.

### Built with

- Semantic HTML5 markup
- CSS custom properties
- Flexbox

### What I learned

- I can control the arrangement of Flexbox by axis - a column or a row. All I need to do is specify it after display: flex.
- Displaying sizes with as vh provides flexibility when aligning nested items. I can create borders around something through padding.

```css
display: flex;
flex-direction: column;
align-items: center;
justify-content: center;
```

### Continued development

Now that I got the hang of panels I want to do more of them. The next challenge is creating a log-in panel.

## Author

- Website - [Vic Kalchev](https://pivotup.co)
- Frontend Mentor - [@vickalchev](https://www.frontendmentor.io/profile/vickalchev)
- Twitter - [@vickalchev](https://www.twitter.com/vickalchev)
