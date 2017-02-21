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
 * Declare variable `items` outside of loop
 * Create `scroll` variable equal to document scroll value
 * Create `pizzas` array to hold created pizzas
 * Revise for loop

You might find the FPS Counter/HUD Display useful in Chrome developer tools described here: [Chrome Dev Tools tips-and-tricks](https://developer.chrome.com/devtools/docs/tips-and-tricks).

### Optimization Tips and Tricks
* [Optimizing Performance](https://developers.google.com/web/fundamentals/performance/ "web performance")
* [Analyzing the Critical Rendering Path](https://developers.google.com/web/fundamentals/performance/critical-rendering-path/analyzing-crp.html "analyzing crp")
* [Optimizing the Critical Rendering Path](https://developers.google.com/web/fundamentals/performance/critical-rendering-path/optimizing-critical-rendering-path.html "optimize the crp!")
* [Optimizing JavaScript](https://developers.google.com/web/fundamentals/performance/critical-rendering-path/adding-interactivity-with-javascript.html "javascript")
* [Measuring with Navigation Timing](https://developers.google.com/web/fundamentals/performance/critical-rendering-path/measure-crp.html "nav timing api"). We didn't cover the Navigation Timing API in the first two lessons but it's an incredibly useful tool for automated page profiling. I highly recommend reading.
* <a href="https://developers.google.com/web/fundamentals/performance/optimizing-content-efficiency/eliminate-downloads.html">The fewer the downloads, the better</a>
* <a href="https://developers.google.com/web/fundamentals/performance/optimizing-content-efficiency/optimize-encoding-and-transfer.html">Reduce the size of text</a>
* <a href="https://developers.google.com/web/fundamentals/performance/optimizing-content-efficiency/image-optimization.html">Optimize images</a>
* <a href="https://developers.google.com/web/fundamentals/performance/optimizing-content-efficiency/http-caching.html">HTTP caching</a>

### Customization with Bootstrap
The portfolio was built on Twitter's <a href="http://getbootstrap.com/">Bootstrap</a> framework. All custom styles are in `dist/css/portfolio.css` in the portfolio repo.

* <a href="http://getbootstrap.com/css/">Bootstrap's CSS Classes</a>
* <a href="http://getbootstrap.com/components/">Bootstrap's Components</a>
