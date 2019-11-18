---
title: BunnyCDN
weight: 40
description: Fast, Low-cost, Custom domain support, Responsive support team from Slovenia
disableToc: true
---

### Pros

 - Fast
 - Low-cost
 - Custom domain support
 - Responsive support team from Slovenia

### Costs

From [$0.01/GB ](https://bunnycdn.com/pricing)

### Deploying to BunnyCDN with WP Static Site Generator

 - [Manual deploy](#manual-deploy-with-the-free-version) Free version
 - [Auto deploy](#auto-deploy-with-the-pro-version) Pro version

#### Manual deploy with the free version

 - select the ZIP deployment method within the plugin's settings
 - set your Base URL to the final domain your users will visit your webite on
 - optionally set any other [configuration](/configuration) options for the crawling, processing or deployment phases 
 - generate your static site and download your resulting ZIP file
 - unzip the folder to a directory under git version control
 - upload your files to BunnyCDN, via their website

BunnyCDN also provides an FTP method to connect and upload your files, if that is preferred.

#### Auto deploy with the Pro version 

 - select the BunnyCDN deployment method within the plugin's settings

![BunnyCDN deployment option](/images/ui/bunncdn_deploy_option.png)

 - configure your [BunnyCDN related deployment options](#bunnycdn-configuration-options-explained)
 - optionally set any other [configuration](/configuration) options for the crawling, processing or deployment phases 
 - hit the **Start static export** button to trigger the automated deployment


{{% notice tip %}}
If it's your first time deploying to BunnyCDN, it's recommended to first upload a sample `index.html` file and verify that it's viewable at the domain you intend your site to be hosted on. This can prevent lost time in re-deployments while getting things working.
{{% /notice %}}

### BunnyCDN configuration options explained

**Base URL**

Set this to the final domain your users will visit your site on. 

**Pull Zone / Storage Zone**

The storage zone, where your files will be deployed to and the pull zone, which sits in front of the storage zone and allows for static site hosting. Afer deployment, a cache invalidation request will be sent to the pull zone, to ensure the latest file changes are visible. Currently, both pull zone and storage zones will need to be set to an identical name, which goes in this field.

**API Key**

These are set in BunnyCDN ans serve as both your API and FTP passwords.

**Subdirectory**

In the case that you wish your website to live within a subdirectory of your BunnyCDN storage zone, include that directory name here, else leave it blank.


{{% notice tip %}}
Did you know, you don't need to save any of your credentials within the plugin if you are exporting via the UI (vs CRON/CLI). Just enter your credentials on the settings page and hit *Start static site export*. If you navigate away from the page, your credentials will not persist. You can also hit the *Reset to default settings* button to clear any settings you've saved for the plugin from your WordPress database.
{{% /notice %}}
