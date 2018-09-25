---
title: What is a static site?
weight: 10
disableToc: true
---

Static websites are super fast under heavy load, secure by design and often free to host.

That sounds great, but still... what are they? How do I know if I already have one?

Are you running WordPress? Then, you don't have a static website. Remember all that jazz about static sites being "super fast under heavy load, secure by design and often free to host"? Sorry, WordPress can't claim any of those bragging rights.

WordPress, as an example of a "dynamic" site, uses a database in the "backend" to store its content. Where a static site usually stores the content directly within the webpage itself, WordPress must fetch this content from the database and insert it into the webpage that your browser "requests" from the "server", it does this using a "server-side" language called PHP. In fact, WordPress is an application written in this PHP language, that sits on your "web server", listening for incoming requests for webpages via your browser, then scurrying off to grab an image from here, a page title from there, a list of top posts from another far off place, then rushing back to try and assemble them and present them to you. Sounds exhausting!

With a static webpage, it's still being served to you by a "web server", but doesn't require an application like WordPress needing to be on duty to greet you at the door. Not needing to ask you what you want and then go searching for it in a dusty back room while you wait, a static site is like an adept mind-reader, able to meet you at the door with a perfectly wrapped parcel of exactly what you asked for. 

Let's illustrate an example request for a page about "Cats in Winter" and what actions may be taken on WordPress to serve you this content:

 - answer the door
 - hear your request
 - go and check the filing cabinet for the "Cats in Winter" document
 - find out where the accompanying photos are and include those 
 - compile a list of other "cat" and "winter" related documents in case you're interested
 - crunch some data on what other people who request "Cats in Winter" are interested in
 - fetch a list of the top 10 articles on the site and include that in your document
 - check there are any scheduled tasks it needs to do right now
 - put a list of emojis in your document, you know, just in case
 - finally, serve your document

And the same request given to a static site server:

 - answer the door
 - hear your request
 - serve you the exact same content, pre-prepared

Now, you're starting to see in our analogy, how a static site can serve requests to thousands of users, where the exact same content, coming from a dynamic site like WordPress will reach a point of failure.

**By what magic does a static website do this?**

A static website is a collection of individual static webpages, each one self-contained and having no knowledge of it's relationship the rest of the site, besides "links", those things you click on to navigate a "website". Each page is thus completely standalone. It may include images and fonts, but it doesn't exert any effort to find them, it simply has a hard-coded reference. If the image exists in the location declared, you'll see it. 

In order to get these nice, self-contained, static pages, someone needs to create them. This was easy when the internet was conceived - it was the only way! Want 5 pages in your website? Open up a text editor and hand-code all the HTML tags (the special language that describes a webpage). Things got easier, with software that would automatically update links when you renamed a page and allow you to work in a WYSIWYG mode, not needing to know any of the HTML syntax. At this point, the resulting output was still a static website. 

But, things evolve, and WordPress has become the most popular tool for creating and serving websites to the world. And for good reason - it's so easy to create content, upload images, collaborate with a team of content writers, add a plugin for feature x, y or z. 

The convenience we gained was paid for in trade-offs of security, performance and cost. 

Above, we've explained how performance is improved by going static. We'll continue to discuss how they're also more secure and how portability of code and lack of complexity allow for free or low-cost hosting.











