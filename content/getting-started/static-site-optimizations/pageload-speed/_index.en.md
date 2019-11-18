---
title: Pageload Speed Improvements
weight: 30
---

You may have used a tool such as [pingdom](https://tools.pingdom.com/) to get a measure of your sites performance, related to the average time for websites to load. Here, we'll outline a few points that can help with your "on-page" speed optimizations. There are other areas "off-page" that we will cover later, such as your DNS resolution, server response times, geo-distributed CDNs and more.

{{% notice tip %}}
Use the WP Path Rewriting configuration option in the plugin to shave off even more bytes per page. ie, instead of `wp-content/themes/twentyseventeen/style.css`, it can automatcially convert to `c/u/t/style.css`. Across all links on all pages, this is a decent saving that is still fairly unique to this plugin.
{{% /notice %}}

Minifying your HTML/CSS/JS for faster page loads
------------------------------------------------

When using WordPress as a static site generator, you get the benefit of
all the plugins available on WordPress's official plugin site. These
include all sorts of things which can aid in speed and other
optimizations for a static site.

HTML/CSS/JS minification in a nutshell
--------------------------------------

Each character of code in a file adds to its size, which translates to
longer wait times for your users to load the page. Google will also
[factor in page load speed] when ranking sites in its search results.

All the more reason to squeeze every ounce of performance out of your
pages by reducing their size. For HTML, this is usually achieved by
stripping whitespace and empty lines that don't affect how the page
appears to the user.

For CSS and JS, things can be optimized even further, by globally
replacing the names used for classes, functions and variables to short
symbols instead of human readable names that take up more characters and
add weight to the code.

This has just been the most basic of overviews on minification -- read
more [here], [here][1] or even [here][2].

Plugins that can help you minimize your code
--------------------------------------------

There are many plugins that do minification available for free. A sample
of those known to work well when using WordPress as a static site
generator are:

-   [Fast Velocity Minify]
-   [Autoptimize]

Depending on your active theme and other changes unique to your
WordPress site, you may need to play with adjusting the settings with
these plugins. If the resulting site is not rendering correctly, try
turning off all minification settings and then turning them back on one
by one until you have as much minification as possible, whilst keeping
your site rendering perfectly.


Need help minifying your WP static site? Just email us at
<help@wp2static.com>.


  [factor in page load speed]: https://webmasters.googleblog.com/2018/01/using-page-speed-in-mobile-search.html
  [here]: https://blog.stackpath.com/glossary/minification/
  [1]: https://en.wikipedia.org/wiki/Minification_(programming)
  [2]: https://developers.google.com/web/fundamentals/performance/optimizing-content-efficiency/optimize-encoding-and-transfer#minification-preprocessing--context-specific-optimizations
  [Fast Velocity Minify]: https://wordpress.org/plugins/fast-velocity-minify/
  [Autoptimize]: https://wordpress.org/plugins/autoptimize/
