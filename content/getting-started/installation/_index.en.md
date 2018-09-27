---
title: Installation
weight: 15
---

Installing the plugin is done just like any other WordPress plugin. If you've done that before, this should be the usual process. If this is your first time, or it's been a while, no worries, we're going to walkthrough the whole process.

There are a few ways you can install this plugin:

 - [from inside your WordPress dashboard's plugin search](#via-dashboard)
 - [by uploading a ZIP file through your WordPress dashboard](#via-dashboard)
 - [using the command line tool, WP-CLI](#via-cli)
 - directly uploading a ZIP/folder to the fileserver
 - via the [Must Use Plugins](https://codex.wordpress.org/Must_Use_Plugins) special directory

As part of the installation, you will also need to [Activate](#activation) the plugin before use.

You can also [Install other versions of the plugin](#installing-other-versions-of-the-plugin), such as the latest development version or an older version, in case something is incompatible with your site in the current official version.

{{% notice tip %}}
This plugin **is** supported on [network/WPMU](https://codex.wordpress.org/Create_A_Network) installations. Just use the same process via the Network Admin's plugins page.
{{% /notice %}}

## Installing via the WordPress dashboard {#via-dashboard}

From your dashboard, go to Plugins > Add New

![Add new plugin](/images/ui/add_new_plugin.png)

Here, you can either search the WordPress “plugin store” or upload a zip file of the plugin.

To install from the plugin store, enter “WP Static Site Generator” or just a keyword like “static” and you should see WP Static Site Generator in first position.

![Plugin search results](/images/ui/plugin_search_results.png)

Click the Install Now button on the top right corner of the plugin by Leon Stafford. Once the installation is complete, the Install Now button will change to say Activate, which you can go ahead and do.

![Activate the plugin](/images/ui/activate_the_plugin.png)


## Installing other versions of the plugin

To install the latest development version of the plugin, you can get the source code from the [GitHub project](http://github.com/leonstafford/wordpress-static-html-plugin/). 

Installing a previous official release is possible, by going to the WP Static Site Generator’s Advanced page on wp.org and choosing from the menu at the bottom of the page.  

To upload either the latest or a particular version of the plugin that you have as a ZIP file, click on the **Uload Plugin** button and locate the ZIP file of the plugin from your computer.

## Installing via WP-CLI {#via-cli}

For advanced users, you can also install WP Static Site Generator via [WP-CLI](https://wp-cli.org/) with `wp plugin install static-html-output-plugin --activate`.

## Activating the plugin {#activation}

If you didn't already do it as part of one of the steps above, go to your WordPress dashboard's Plugins page, find **WP Static Site Generator** from the list of plugins and click the **Activate** link to enable it for use.
After activation, you can opt-in to improve the plugin’s performance.

![Opt-in](/images/ui/opt_in.png)

That’s it! You’re already to start generating your static site using the plugin.

Be sure to continue reading through the documentation, to ensure the best resulting website in terms of performance, security and cost.
