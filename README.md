## Website Performance Optimization Project

The objective for this project was to optimize the online portfolio for speed. In particular, I was asked to optimize the critical rendering path and make the page render as quickly as possible by applying the techniques learned in the [Critical Rendering Path course](https://www.udacity.com/course/ud884).


### My Optimization Process

####Part 1: Optimize PageSpeed Insights score for `index.html`

* Create thumb images for project list on main page
* Compress all Images
* Inline critical resources (minified) above-the-fold
* Async script tags
* Create WebFont loader
* Reposition all render blocking to end of document


####Part 2: Optimize Frames per Second in `pizza.html`

* Remove FX `determineDx`
* Revise FX `changePizzaSizes` _(line 427)_
 * Create new variable `newWidth`
 * Add case statement to FX
 * Replace `querySelectorAll` with `getElementsByClassName` for efficiency within the DOM
 * Remove references to deleted FXs, create new for loop to change pizza sizes
* Revise FX `updatePositions` _(line 491)_
 * Replace `querySelectorAll` with `getElementsByClassName` for efficiency within the DOM
 * Replace `.mover` with `mover`
 * Declare variables `pizza`, `scroll`, and `pizzaArray` outside of loop
 * Revise for loop


### Customization with Bootstrap
The portfolio was built on Twitter's <a href="http://getbootstrap.com/">Bootstrap</a> framework. All custom styles are in `dist/css/portfolio.css` in the portfolio repo.

* <a href="http://getbootstrap.com/css/">Bootstrap's CSS Classes</a>
* <a href="http://getbootstrap.com/components/">Bootstrap's Components</a>
