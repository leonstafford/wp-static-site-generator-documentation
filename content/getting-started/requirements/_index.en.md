---
title: Requirements
weight: 10
disableToc: true
---

### You’ll need a WordPress installation!

That may go without saying, but this is a WordPress plugin, not a standalone product.

If you don’t have a WordPress site yet, fear not, you can set one up for free on your own computer or get a hosting plan from somewhere like WP Engine. You can always change where you host your WordPress site – another advantage of using WordPress as a static site generator is the ease at which you can move your WordPress installation without causing any downtime for your actual website.

#### Hosting WordPress locally

This is a safe way to host your WordPress site, away from the public and with all the power of your laptop/desktop/raspberryPi, etc!

Some popular tools for setting up a WordPress instance locally (on your own computer):

 - [AMPPS](https://www.ampps.com/) (Linux/Mac/Windows)
 - [Bitnami WordPress Stack](https://bitnami.com/stack/wordpress) (Linux/Mac/Windows)
 - [XAMPP](https://www.apachefriends.org/index.html) (Linux/Mac/Windows)
 - [MAMP](https://www.mamp.info) (Mac/Windows)
 - [Local by Flywheel](https://local.getflywheel.com/) (Mac/Windows)
 - [DesktopServer](https://serverpress.com/get-desktopserver/) (Mac/Windows)

_some Windows hosting environments currently have issues with the plugin, due to Windows-style filepaths not being supported. AMPPS, at least, is known to work fine._

And these, more developer focused products:

 - [VVV](https://github.com/Varying-Vagrant-Vagrants/VVV) (Linux/Mac/Windows)
 - [Docker](https://hub.docker.com/_/wordpress/) (Linux/Mac/Windows)
 - [Beetbox](https://github.com/beetboxvm/beetbox) (Linux/Mac/Windows)
 - [Visible WordPress Starter](https://github.com/visiblevc/wordpress-starter) (Linux/Mac/Windows)

### Recommended hosting for WordPress development servers

We're not a fan of hosting production websites using WordPress, it's why this plugin was created.

With this plugin, you can hopefully say goodbye to overpriced, underperforming web hosting. If you can't get away with just a local WP installation and need remote access to it, ie for collaborative content editing with a team, the below options and affordable, professional options we can recommend for the purpose of hosting a WordPress development server.  

 - [Digital Ocean](https://www.digitalocean.com)
 - [Amazon LightSail](https://aws.amazon.com/lightsail/)

In general, try to avoid paying any more than $5/month for a development WordPress server. The above options have professional tooling support, allow for installation of custom software, SSH connections, SSL certificates and Pay-As-You-Go pricing.

### PHP Version

Whilst the plugin may activate on PHP versions less than 5.4, we'd recommend you use at least version 7.1. For PHP 5.x users, upgrading to at least 5.6 is recommended, though this is no longer supported after the end of 2018.


### PHP Extensions

 - cURL
 - ZIP

### PHP XML Support

Usually already installed and often provided on Linux servers with the `php-xml` package.

### Web server

The plugin should work with any webserver you are using, such as Apache or nginx.






