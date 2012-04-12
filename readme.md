# jQuery Scroll Depth
This is a jQuery plugin that keeps an eye on how far down the page a user has scrolled and then reports data back to Google Analytics using the GA Events API. The default behavior reports on the 25%, 50%, 75%, and 100% scroll marks. It also sends an initial "Baseline" event to use as a benchmark.

In addition to the percentage scroll marks you can trigger events based on specific DOM elements. For example you can tell the plugin to report whenever the article comments div is scrolled into view, or whenever the footer is reached.

Data is sent to Google Analytics so it's required that you have Google Analytics tracking implemented on your site.

[View the Project Page](http://robflaherty.github.com/jquery-scrolldepth/)

[View the Blog Post](http://www.ravelrumba.com/blog/tracking-scroll-depth-jquery-google-analytics/)

## Usage
```javascript
// Basic
$.scrollDepth();

// With some options
$.scrollDepth({
  minHeight: 2000, // Only track for documents taller than 2000px | Default: 0
  elements: ['#comments', 'footer'] // Track DOM elements | Default: []
  percentage: false, // Don't track depth percentage | Default: true
});
```
## GA Events Warning
<del>GA Events data messes with your bounce rate.</del> As of version 0.1.1 of this plugin, the scroll events no longer impact your bounce rate. If you downloaded the initial 0.1.0 release and you care about the GA displayed bounce rate, update to the latest version.

## Browser Support
Tested in Chrome (18), Firefox (8), Safari (5), Opera (10), IE (7-10). Also tested on iOS, Opera Mobile, and a few Android emulators.

## Contact
If you have any questions please leave a comment on the [associated blog post](http://www.ravelrumba.com/blog/tracking-scroll-depth-jquery-google-analytics/) or find me on Twitter at [@robflaherty](https://twitter.com/#!/robflaherty).

## Changelog

0.1.1 (4/12/12): Added `opt_noninteraction` option to GA event to avoid impacting bounce rate.

0.1 (4/7/12): Initial release.

## License
Licensed under the MIT and GPL licenses.