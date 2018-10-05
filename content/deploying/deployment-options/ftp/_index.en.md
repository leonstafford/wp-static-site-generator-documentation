---
title: FTP
weight: 50
description: Flexible method for deploying to most traditional servers
disableToc: true
---

Deploying to a remote server via FTP
------------------------------------

For this example, we'll use 2 domains:

-   **https://mywpsite.com** to represent our server that runs WordPress
    (could be your local computer as http://localhost/,
    http://mysite.local, http://192.168.0.1/, on WP Engine, Digital
    Ocean, or other hosting). 
-   **https://mystaticsite.com** to represent where you're deploying
    your static site to. This will end up being where you want your
    users to visit, so your production domain, but during testing, you
    may set this to a staging server, such
    https://staging.mystaticsite.com, http://198.143.164.252 or to a
    subfolder such as https://mystaticsite.com/myfirststatictest/. 

The FTP deployment method is quite simple in the options you need to
fill out. Below, we see an example of what your settings might look like
and we'll go through what each option does:

![][1]

Base Url
--------

*Beware -- be careful not to overwrite your WordPress site with your
static site. This can be a pain to cleanup and may even cause your site
to be inaccessible until cleaned. The main thing to avoid is setting
your Base Url to the same address as your WordPress site. If it's the
same domain, but a different subdomain or subdirectory, that's fine,
though.*

Set your Base Url to what we defined at the top of this page as
https://mystaticsite.com or your equivalent. 

FTP Server
----------

Set this to what you would use in what's usually called the *host* or
*server address* field in your FTP program. Often, it's the same as your
domain, or with the *ftp* subdomain in front of it. Other times,
especially if you're setting up a new site and don't have your domain
yet, it will be an IP address.

FTP Username
------------

Again, the same username as what you would use to connect via
[FileZilla], Cyberduck or whatever app you like to use for FTP.  

FTP Password
------------

As above. This will not be shown as you enter it, so if you have a
tricky password that you need to enter manually, you can type it
somewhere else that you can see it, such as the browser's address bar
and then copy and paste it in. Be careful not to copy any space
characters at the start or end of your password as this may cause them
to be interpreted as part of your actual password characters. 

FTP Remote Path
---------------

This may not be intuitive as to what you need to set here, so we advise
to first do a test upl

  [1]: /images/ui/ftp_settings.png
  [FileZilla]: https://filezilla-project.org/


{{% notice tip %}}
Did you know, you don't need to save any of your credentials within the plugin if you are exporting via the UI (vs CRON/CLI). Just enter your credentials on the settings page and hit *Start static site export*. If you navigate away from the page, your credentials will not persist. You can also hit the *Reset to default settings* button to clear any settings you've saved for the plugin from your WordPress database.
{{% /notice %}}
