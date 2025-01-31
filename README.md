# Splide
[Splide](https://splidejs.com/) is a lightweight, powerful and flexible slider and carousel, written in pure JavaScript without any dependencies.

* [Demo](https://splidejs.com/)
* [Documents](https://splidejs.com/category/users-guide/)

## Features
* Pure JavaScript without any dependencies
* Small size, less than 26kB(10kB gzipped)
* Flexible and extensible
* Multiple slides
* Slide or fade transition by CSS
* Responsive, supporting breakpoints
* Accepting CSS relative units, such as vw, %, rem, etc
* No need to crop images
* Autoplay with progress bar and play/pause buttons
* "Right to left" and vertical direction
* Mouse drag and touch swipe
* Nested slider
* Lazy loading
* Thumbnail slider
* Accessibility friendly, supporting keyboard control and ARIA attributes
* Internet Explorer 10

## Installation
There are 3 ways to install the Splide on your site.
* NPM
* Download
* CDN

Only the NPM way is explained in the following steps. Visit [this page](https://splidejs.com/getting-started/) for other methods.

1. Get the latest version by NPM:
    ```bash
    $ npm install @splidejs/splide
    ```
1. Link to the stylesheet:
    ```html
    <link rel="stylesheet" href="node_modules/@splidejs/splide/dist/css/splide.min.css">
    ```
1. Write HTML for building a slider:
    ```html
    <div id="splide" class="splide">
      <div class="splide__track">
        <ul class="splide__list">
          <li class="splide__slide">Slide 01</li>
          <li class="splide__slide">Slide 02</li>
          <li class="splide__slide">Slide 03</li>
        </ul>
      </div>
    </div>
    ```
1. Initialize Splide. The selector accepts an ID, a class name or an Element itself:
    ```javascript
    import Splide from '@splidejs/splide';
    new Splide( '#splide' ).mount();
    ```
    Note that only the first element will be initialized even if using a class name.

## Options
### Changing Options
Pass an object to the second argument of the ```Splide``` constructor:
```javascript
new Splide( '#splide', {
  type   : 'loop',
  perPage: 3,
} );
```
Or set a ```data-splide``` attribute to a root element in a JSON format: 
```html
<div id="splide" class="splide" data-splide="{"type":"loop","perPage":3}">
</div>
```
### Available Options
Here is a list of options and brief explanations. Visit [this page](https://splidejs.com/options/) for more details.

* **type**: Determine a slider type.
* **rewind**: Whether to rewind a slider before the first slide or after the last one.
* **speed**: Transition speed in milliseconds.
* **width**: Define slider max width.
* **height**: Define slider height.
* **fixedWidth**: Fix width of slides.
* **fixedHeight**: Fix height of slides.
* **heightRatio**: Determine height of slides by ratio to a slider width.
* **perPage**: Determine how many slides should be displayed per page.
* **perMove**: Determine how many slides should be moved when a slider goes to next or previous page.
* **start**: Start index.
* **focus**: Determine which slide should be focused.
* **gap**: Gap between slides.
* **padding**: Set padding-left/right in horizontal mode or padding-top/bottom in vertical one.
* **easing**: Animation timing function for CSS transition.
* **arrows**: Whether to append arrows.
* **arrowPath**: Change the arrow SVG path.
* **pagination**: Whether to append pagination(indicator dots).
* **autoplay**: Whether to enable autoplay.
* **interval**: Autoplay interval in milliseconds.
* **pauseOnHover**: Whether to stop autoplay while a slider is hovered.
* **pauseOnFocus**: Whether to stop autoplay while a slider elements are focused.
* **lazyLoad**: Enable lazy load for images.
* **preloadPages**: Determine how many pages around an active slide should be loaded beforehand. This only works the lazyLoad option is “nearby”.
* **keyboard**: Whether to control a slider via keyboard.
* **drag**: Whether to allow mouse drag and touch swipe.
* **flickThreshold**: Threshold for determining if the action is “flick” or “swipe”.
* **flickPower**: Determine power of flick. The larger number this is, the farther a slider runs by flick.
* **flickMaxPages**: Limit a number of pages to move by flick.
* **direction**: Slider direction.
* **cover**: Whether to convert an img src to background-image of its parent element. height, fixedHeight or heightRatio is required.
* **accessibility**: Whether to enable accessibility(ARIA attributes) or not.
* **isNavigation**: Determine if a slider is navigation for another.
* **trimSpace**: Whether to trim spaces before the fist slide or after the last one.
* **breakpoints**: Breakpoints definitions.
* **classes**: Collection of class names.
* **i18n**: Collection of texts for i18n.

## API and Extension
Splide provides some APIs and the way to customize the behaviour programmatically.
* [APIs](https://splidejs.com/apis/)
* [Extension](https://splidejs.com/extension/)

## License
Splide is released under the MIT license.  
© 2019 Naotoshi Fujita