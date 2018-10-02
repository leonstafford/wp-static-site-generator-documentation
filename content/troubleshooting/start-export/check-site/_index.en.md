---
title: Check site
weight: 20
---

My exported site looks weird – missing styles/images, etc
---------------------------------------------------------

This is the most common issues new users of the plugin face, or even veteran fans of the plugin, once they’ve switched to a new theme or made some other changes to their site. 
The reason for these missing web assets (images, stylesheets, etc) are that they weren’t “discovered” during the crawling process that the plugin uses to generate a static copy of your WordPress site. 
Crawling / spidering

The process the plugin uses to create a copy of your website is the same mechanism that search engines have used since the dawn time (well, important time – the internet era!). Their software will start with an index to your website, usually the “naked” domain, ie https://mywpsite.com, where it looks at the source code (right-click on any webpage and choose “View source” to see what it’s looking at). From this source code, it will scan for any other links on that site and add it to its list of pages to crawl (also known as spidering). Each subsequent page in the site it crawls, it looks at all the links within and skips any already done, else continues crawling until it finds no more new links.
WP Static Site Generator works much the same way. It looks in the source code of your site’s homepage and starts crawling all links it thinks are a part of your website.  The crawler is only as smart as the code that commands it though, so we try to help it out by handing it a list of all the URLs to your site’s posts and pages. We also ask it to grab all the media in your WP uploads directory and theme folder.

> This works for 99% of cases.

The 1% (of missing files)
-------------------------

For any files that the plugin doesn’t manage to auto-include in its crawling, we can open the Advanced Settings section in the plugin’s settings and give it instructions to forcible include any files we add (one per line, no commas), as such:

![Additional URLs to include](/images/ui/additional_urls.png)

The above works great, providing you know which files are missing from your export.

Identifying which files are missing and need to be forcibly included
--------------------------------------------------------------------

Sometimes, it’s obvious or you know your theme intimately, so can tell what’s missing from the export. For other cases, you will need to look at the exported static site in your browser, open the browser’s console and find any missing files. These may show either in the JavaScript console or, for example, in Chrome/Chromium, they can show in the Network console. 

Once you have identified which assets are missing on the static site, for example:

``` wp-block-code
https://mystaticsite.com/content/ui/theme/custom_logo.jpg
```

You will likely need to translate the URL back to the original WP site’s URL, as one of WP Static Site Generator’s features is to strip any trace of WordPress from your exported site. One way it does this is to rename obvious WP folders, like *wp-content*. The default setting (which you can override) renames this folder to *contents*. You can see the full rewrite rules and modify them under Advanced Settings. 
For the above example, if we have the default rewriting settings enabled, we would need to add under Additional URLs:

``` wp-block-code
https://mywpsite.com/contentss/themes/twentyseventeen/custom_logo.jpg
```

Improving our crawling mechanism so that you don’t have to manually intervene
-----------------------------------------------------------------------------

The Additional URLs field was created as a quick solution to the problem of assets that failed to load. With the increase in assets dynamically loaded via JavaScript (our crawler is not JavaScript aware… yet), it has seen increased usage.
There is still loads of room for improvement in our crawler – so by all means, please use the Additional URLs field to overcome any imperfect exports, but then, please [let us know](https://wp2static.com/community/) what theme you’re using, what assets were missing from your export and any related customizations to your WordPress setup that you think may factor in. With this, we can come up with an improvement to the crawling mechanism for you and no doubt other users with a similar setup will also benefit. 
If you’re a nifty programmer, you can also make the improvements as a pull request to our [project on GitHub](https://github.com/leonstafford/wordpress-static-html-plugin).
