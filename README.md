# Huddle Landing Page With Curved Section

<p align="left">
  <img src="https://img.shields.io/badge/Difficulty-Junior-brightgreen?style=for-the-badge&logo=frontendmentor" alt="Difficulty">
  <img alt="GitHub repo size" src="https://img.shields.io/github/repo-size/vanzasetia/huddle-landing-page-with-curved-section?style=for-the-badge&logo=github">
  <a href="https://twitter.com/vanzasetia" target="_blank"><img src="https://img.shields.io/twitter/follow/vanzasetia?logo=twitter&style=for-the-badge" alt="Twitter followers." /></a>
  <img alt="GitHub last commit" src="https://img.shields.io/github/last-commit/vanzasetia/huddle-landing-page-with-curved-section?style=for-the-badge&logo=git">
  <img alt="Netlify" src="https://img.shields.io/netlify/?style=for-the-badge&logo=netlify">
</p>
<p>
  <a href="http://jigsaw.w3.org/css-validator/check/referer">
    <img style="border:0;width:88px;height:31px"
        src="http://jigsaw.w3.org/css-validator/images/vcss-blue"
        alt="Valid CSS!" />
    </a>
</p>

## Feedback and Live Review
* [🌍 Live Review](https://vanzahuddlecurved.netlify.app/)
* [👉 Give feedback on Frontend Mentor platform]()
* [🐦 Give Feedback on Twitter]()

## Table of contents
- [Story](#the-story-when-doing-this-challenge)
  - [When I Build the Header](#header)
  - [When I Build the Hero Section](#hero)
  - [When I Build the Section](#section)
  - [When I Build the Footer](#footer)
- [What I Learned](#what-i-learned)
- [Technology that I used](#built-with)
- [Useful Resources](#useful-resources)
- [Continued Development](#continued-development)

## The Story When Doing This Challenge
This is my story when building this project. I want to mention that `style-guide.md` doesn't provide the blue color as the active state of the social media icons. So, I used color picker and get this color code `rgb(8, 193, 255)`.

I also used very dark cyan color as my main font color.

### Header
I noticed that the logo and the *try it free* button on mobile design is too small. I made them a little bit bigger. It's also an accessibility part where if your website has buttons, they need to have a decent *touch target*. That way they are easy to click.

## Hero
When I built the hero section, I noticed that `16px` body font size is too big, so I reduced it to `15px`.

### Section
The `section-background` was tricky. After several try and error, I found out that I need to put the `background-image` on the sibling element, not the direct section. 

Let me explain, what's that mean. For example I wanted the first section have `bg-section-top-1` and `bg-section-bottom-2`. I wanted the top one on the top and so the opposite. At first I thought that I need to put those background on its section and then position it using `background-position`.

```css
.section {
  background-image: 
    url("../images/bg-section-top-mobile-1.svg"),
    url("../images/bg-section-bottom-mobile-1.svg")
  ;
  background-position: top, bottom;
  background-repeat: no-repeat;
  background-size: 100%;
}
```

But it doesn't work, the background images were inside the section. They also were invisible, since I used the same color for background color.

So, I tried to put it on the previous sibling, which was `hero` and it worked!

```css
.hero {
  background-image: 
    url("../images/bg-section-top-mobile-1.svg"),
  ;
  background-position: bottom;
  background-repeat: no-repeat;
  background-size: 100%;
}
```

For the bottom background image I used the next sibling element.

### Footer

## What I Learned



## Built With
This project is created using **HTML5**, **CSS3**, and **Sass**. 

I used one of the form features from [Netlify which Forms Spam Filters](https://docs.netlify.com/forms/spam-filters/), using **Honeypot field**.

I also used [Mailgo](https://mailgo.dev/), which is a light JavaScript library for `mailto` and `tel`. It will give you a nice popup for every `mailto` and `tel` link. I really ❤️ love this library, since it is **easy** and **simple** to use.
<p align="left">
  <img src="https://raw.githubusercontent.com/devicons/devicon/master/icons/html5/html5-original.svg" alt="" width="auto" height="70px">
  <img src="https://raw.githubusercontent.com/devicons/devicon/master/icons/css3/css3-original.svg" alt="" width="auto" height="70px">
  <img src="https://raw.githubusercontent.com/devicons/devicon/master/icons/sass/sass-original.svg" alt="" width="auto" height="70px">
  <img src="./images/mailgo.png" alt="" width="auto" height="70px">
</p>

## Useful Resources
* [Optimize Cumulative Layout Shift](https://web.dev/optimize-cls/)
* [Form Validation UX in HTML and CSS](https://css-tricks.com/form-validation-ux-html-css/)
* [Font Converter from any format to any format that you want](https://www.fontconverter.io/en)
* [ Footer Tag | MDN Web Docs](https://developer.mozilla.org/en-US/docs/Web/HTML/Element/footer#accessibility_concerns)

## Continued development
I will take people feedback and improve this solution.