---
title: Netlify
weight: 20
description: FREE, Custom domain support, The specialists in static website hosting
disableToc: true
---

### Pros

 - FREE
 - Custom domain support
 - The specialists in static website hosting


### Costs

Free and [paid plans](https://www.netlify.com/pricing/)

### Official static web hosting guide

[A Step-by-Step Guide: Deploying A Static Site or Single-page Ap ](https://www.netlify.com/blog/2016/10/27/a-step-by-step-guide-deploying-a-static-site-or-single-page-app/)

### Deploying to Netlify with WP Static Site Generator

 - [Manual deploy](#manual-deploy-with-the-free-version) Free version
 - [Auto deploy](#auto-deploy-with-the-pro-version) Pro version

#### Manual deploy with the free version

 - select the ZIP deployment method within the plugin's settings
 - set your Base URL to the final domain your users will visit your webite on
 - optionally set any other [configuration](/configuration) options for the crawling, processing or deployment phases 
 - generate your static site and download your resulting ZIP file
 - drag and drop your ZIP file into the Netlify UI to deploy


{{% notice note %}}
TIP: For easier deployments via the ZIP (or even the "Test deploy" method), consider setting up a Git repository on GitHub, GitLab, BitBucket or any others supported by Netlify. Then when you push changes to the repo, Netify will automatically build it for you!
{{% /notice %}}

#### Auto deploy with the Pro version 

 - select the Netlify deployment method within the plugin's settings

![Netlify deployment option](/images/ui/netlify_deploy_option.png)

 - configure your [Netlify related deployment options](#netlify-configuration-options-explained)
 - optionally set any other [configuration](/configuration) options for the crawling, processing or deployment phases 
 - hit the **Start static export** button to trigger the automated deployment


{{% notice note %}}
TIP: If it's your first time deploying to Netlify, you can just take your ZIP file and drag it onto the UI at Netlify to create your Netlify site, then configure any settings within Netlify. This will work best if you've chosen to export with relative links set, so that the site's URLs will work wherever deployed.
{{% /notice %}}

### Netlify configuration options explained

**Base URL**

Set this to the final domain your users will visit your site on. If you're just getting started you can set it to your Netlify site's URL, ie https://mystaticsite.netlify.com

**Personal Access Token**

You can create this here on [Netlify](https://app.netlify.com/account/applications/personal).

**Site ID**

This will be what's shown in a few places within the Netlify UI for your site, as shown here:

![Netlify Site ID](/images/ui/netlify_site_id.png)





{{% notice note %}}
TIP: Did you know, you don't need to save any of your credentials within the plugin if you are exporting via the UI (vs CRON/CLI). Just enter your credentials on the settings page and hit *Start static site export*. If you navigate away from the page, your credentials will not persist. You can also hit the *Reset to default settings* button to clear any settings you've saved for the plugin from your WordPress database.
{{% /notice %}}
