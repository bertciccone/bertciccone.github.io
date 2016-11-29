frontend-nanodegree-mobile-portfolio
====================================

## Website Performance Optimization portfolio project

# Getting Started

The optimized pages can be run from: [Run Portfolio](https://bertcuda.github.io/frontend-nanodegree-mobile-portfolio/index.html).
Sources can be downloaded from: [Get Sources](https://bertcuda.github.io/frontend-nanodegree-mobile-portfolio/).
README.md can be downloaded from: [Get README](https://bertcuda.github.io/frontend-nanodegree-mobile-portfolio/README.md).

The following optimizations were implemented. (You can search for the following comments in the code files.)

# Optimizations: Portfolio Loading
index.html:
perf: media = screen
perf: replace complex css selectors with simple classes and eliminate unused css
perf: move scripts after body (1 pt improvement)
perf: load web font asynchronously
perf: print media query
perf: move inline analytics js to file
perf: async on analytics script

# Optimizations: Changing Pizza Sizes
main.js:
perf: resize pizzas using a constant percentage
perf: use getElementsByClassName and move outside of loop [REVIEW SUGGESTION]
perf: move getElementByID outside of loop [REVIEW SUGGESTION]
perf: reduce size and optimize pizzeria image

# Optimizations: Pizza Scrolling
main.js:
perf: query and save scrollTop to prevent repeated accesses in loop
perf: use saved mover elements
perf: requestAnimationFrame before updating movers
perf: save mover elements to prevent repeated queries
perf: reduced size of the moving pizza image file
perf: move movingPizzas1 querySelector outside of loop
perf: only create moving pizzas that fit in visible window
perf: pre-calculate phase values [REVIEW SUGGESTION]
perf: calculate the number of pizzas needed [REVIEW SUGGESTION]
perf: set style.left to get ready to use translateX in updatePositions [REVIEW SUGGESTION]
perf: use will-change: transform and translateX for faster repositioning [REVIEW SUGGESTION]
Alternate optimization:
perf: use backface-visibility: hidden [REVIEW SUGGESTION]

# Optimizations: General
pizza.html:
perf: inline css

## ORIGINAL README CONTENT

## Website Performance Optimization portfolio project

Your challenge, if you wish to accept it (and we sure hope you will), is to optimize this online portfolio for speed! In particular, optimize the critical rendering path and make this page render as quickly as possible by applying the techniques you've picked up in the [Critical Rendering Path course](https://www.udacity.com/course/ud884).

To get started, check out the repository and inspect the code.

### Getting started

####Part 1: Optimize PageSpeed Insights score for index.html

Some useful tips to help you get started:

1. Check out the repository
1. To inspect the site on your phone, you can run a local server

  ```bash
  $> cd /path/to/your-project-folder
  $> python -m SimpleHTTPServer 8080
  ```

1. Open a browser and visit localhost:8080
1. Download and install [ngrok](https://ngrok.com/) to the top-level of your project directory to make your local server accessible remotely.

  ``` bash
  $> cd /path/to/your-project-folder
  $> ./ngrok http 8080
  ```

1. Copy the public URL ngrok gives you and try running it through PageSpeed Insights! Optional: [More on integrating ngrok, Grunt and PageSpeed.](http://www.jamescryer.com/2014/06/12/grunt-pagespeed-and-ngrok-locally-testing/)

Profile, optimize, measure... and then lather, rinse, and repeat. Good luck!

####Part 2: Optimize Frames per Second in pizza.html

To optimize views/pizza.html, you will need to modify views/js/main.js until your frames per second rate is 60 fps or higher. You will find instructive comments in main.js.

You might find the FPS Counter/HUD Display useful in Chrome developer tools described here: [Chrome Dev Tools tips-and-tricks](https://developer.chrome.com/devtools/docs/tips-and-tricks).

### Optimization Tips and Tricks
* [Optimizing Performance](https://developers.google.com/web/fundamentals/performance/ "web performance")
* [Analyzing the Critical Rendering Path](https://developers.google.com/web/fundamentals/performance/critical-rendering-path/analyzing-crp.html "analyzing crp")
* [Optimizing the Critical Rendering Path](https://developers.google.com/web/fundamentals/performance/critical-rendering-path/optimizing-critical-rendering-path.html "optimize the crp!")
* [Avoiding Rendering Blocking CSS](https://developers.google.com/web/fundamentals/performance/critical-rendering-path/render-blocking-css.html "render blocking css")
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
