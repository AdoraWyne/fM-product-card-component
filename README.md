# Frontend Mentor - Product preview card component solution

This is a solution to the [Product preview card component challenge on Frontend Mentor](https://www.frontendmentor.io/challenges/product-preview-card-component-GO7UmttRfa). Frontend Mentor challenges help you improve your coding skills by building realistic projects. 

## Overview

### The challenge
1. I did not how to change the image based on the screen size as desktop screen and mobile screen using different images.

  Solution: 

  Utilised ```<picture>```.

  When the screen is at least 600px long, it will change the image to the desktop version.
  Understand more about [picture tag here](https://www.youtube.com/watch?v=Rik3gHT24AM&t=0s).
  ```html
    <picture>
      <source srcset="images/image-product-desktop.jpg" media="(min-width: 600px)">
      <img src="images/image-product-mobile.jpg" alt="mobile pic">
    </picture>
  ```


2. For the price container, after I made the sale-price's font size bigger, I'm not sure how to make the original-price stay align in the middle with the sale-price.

  Solution: Duh. Solution is so easy!!! Only added ```align-items: center``` (I have already made price container a flexbox before this).

3. How to add the svg icon? My initial approach was using <img> tag.

  But I can do this:

  On HTML:
  ```html
  <button data-icon="shopping-cart">Add to Cart</button>
  ```

  On CSS:

  - Used pseudo code here, therefore need to use ```content: ''```.
  - The width and height were given by the style guide.
  ```css
  button[data-icon="shopping-cart"]::before {
    content: "";
    background-image: url("images/icon-cart.svg");
    width: 15px;
    height: 16px;
  }
  ```

### Links

- Solution URL: [My Solution on Github](https://github.com/AdoraWyne/fM-product-card-component)
- Live Site URL: [Live Site](https://adorawyne.github.io/fM-product-card-component/)

## My process
1. I built with the mobile version first and started my code from up to bottom: from the image to the button.
2. Before jumping into CSS, I structured my HTML file first.
3. On CSS:
    - Imported the font family.
    - Setup the border-box for box-sizing and margin&padding to 0.
    - General styling for the ```<body>```
    - Then tackle each container/tag/class to style.

However, I was not happy with my thought process so I sought for a video tutorial to improve my way of approach this challenge. (Link above)

### Built with

- Semantic HTML5 markup
- CSS custom properties
- Flexbox
- CSS Grid
- Mobile-first workflow

### What I learned

Use this section to recap over some of your major learnings while working through this project. Writing these out and providing code samples of areas you want to highlight is a great way to reinforce your own knowledge.

To see how you can add code snippets, see below:

```html
<h1>Some HTML code I'm proud of</h1>
```
```css
.proud-of-this-css {
  color: papayawhip;
}
```
```js
const proudOfThisFunc = () => {
  console.log('🎉')
}
```

### Continued development

Use this section to outline areas that you want to continue focusing on in future projects. These could be concepts you're still not completely comfortable with or techniques you found useful that you want to refine and perfect.

**Note: Delete this note and the content within this section and replace with your own plans for continued development.**

### Useful resources

- [CSS Tricks - Flexbox](https://css-tricks.com/snippets/css/a-guide-to-flexbox/) - This helped me understand Flexbox more especially the image about the main axis & cross axis.
- [Kevin Powell Solution](https://www.youtube.com/watch?v=B2WL6KkqhLQ) - Kevin's way of approaching this challenge is amazing and the way he explains is easy to follow along. I learned a lot from this.

## Author

- Website - [Adora Kong](https://adora-chin-ying.vercel.app/)
- Frontend Mentor - [@yourusername](https://www.frontendmentor.io/profile/yourusername)
- Twitter - [Adora](https://twitter.com/adoraflowerbeee)

## Acknowledgments

Big applause to Kevin Powell (and myself!).

