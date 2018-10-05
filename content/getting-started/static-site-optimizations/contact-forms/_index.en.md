---
title: Contact forms
weight: 10
---

Contact form solutions for static websites
------------------------------------------

One of the most widely used WordPress plugins is the Contact Form 7
plugin. 

Install it, add a shortcode to a page(s) *et voila*, you have a working
contact form for your website. This is great, until you start getting
all the spam email abuse, even with reCAPTCHA enabled, but I digress.

When you start using WordPress as a static site generator, one of the
first things you miss is this easy contact form implementation.  

Is it harder to add a contact form to a static site?
----------------------------------------------------

It doesn't have to be. In many cases, it can even be easier, as you are
just pasting a bit of code into your page, like you did before with
shortcodes, but this time, you don't need to install and activate a
plugin and ensure it's up to date.

3rd party form / form submission providers for your static website
------------------------------------------------------------------

These are some of the most popular form solutions for static websites.
There are countless others out there of varying quality.

-   [Formspree]
-   [Simple Form]
-   [Netlify]
-   [FormKeep]
-   [EmailMeForm]
-   [99Inbound]
-   [DateFire]
-   [Zapier] \| [guide]

Each of the above has slightly different ways to implement, by either
making slight tweaks to your existing form's code, embedding a whole
other form or by wiring a few online services to make your own end to
end solution. Check this page again, as more example implementations
will be added for each vendor. 

Advanced mailto link with a full form
-------------------------------------

You can also use a little JavaScript to capture the [contents of a form
and create a mailto link] that has the recipient, subject and body
pre-populated for all mail clients to understand, such as:

``` {.wp-block-code}
mailto:help@wp2static.com?subject=Question%20about%20contact%20forms&body=Hi%20there%2C%20I%20just%20read%20your%20article%20about%20contact%20forms%20and%20want%20to%20ask%20you%20further%20questions.%20When%27s%20a%20good%20time%20to%20chat%3F
```

When the above link is clicked, it will create an email in your default
email client that looks like this:

![][1]

  [Formspree]: https://formspree.io/
  [Simple Form]: https://getsimpleform.com/
  [Netlify]: https://www.netlify.com/docs/form-handling/
  [FormKeep]: https://formkeep.com/
  [EmailMeForm]: https://www.emailmeform.com/
  [99Inbound]: https://www.99inbound.com/
  [DateFire]: https://app.datafire.io/
  [Zapier]: https://zapier.com/
  [guide]: https://bowtie.io/help/connect-contact-form-to-zapier/
  [contents of a form and create a mailto link]: https://www.webdeveloper.com/forum/d/229947-javascript-mailto-form
  [1]: /images/clickingadvancedmailto.png






