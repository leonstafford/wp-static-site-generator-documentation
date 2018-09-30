---
title: GitHub Pages
weight: 30
description: FREE, Custom domain support
disableToc: true
---

### Pros

 - FREE
 - Custom domain support

### Costs

Free

### Official static web hosting guide

[GitHub Pages Basics](https://help.github.com/categories/github-pages-basics/)

### Deploying to GitHub Pages with WP Static Site Generator

 - [Manual deploy](#manual-deploy-with-the-free-version) Free version
 - [Auto deploy](#auto-deploy-with-the-pro-version) Pro version

#### Manual deploy with the free version

 - select the ZIP deployment method within the plugin's settings
 - set your Base URL to the final domain your users will visit your webite on
 - optionally set any other [configuration](/configuration) options for the crawling, processing or deployment phases 
 - generate your static site and download your resulting ZIP file
 - unzip the folder to a directory under git version control
 - `git add .`
 - `git comit -m "new version of my static site"`
 - `git push` 

Use a GUI git tool instead of the command line method above if you prefer.

{{% notice tip %}}
For easier deployments via the ZIP/test deploy method, consider linking the latest export directory the plugin generates (symlinked to `latest-export` in your Working Directory) to your GitHub repo. Then you don't need to download anything off your WordPress server to commit and deploy!
{{% /notice %}}

#### Auto deploy with the Pro version 

 - select the GitHub Pages deployment method within the plugin's settings

![GitHub Pages deployment option](/images/ui/github_pages_deployment_method.png)

 - configure your [GitHub Pages related deployment options](#github-pages-configuration-options-explained)
 - optionally set any other [configuration](/configuration) options for the crawling, processing or deployment phases 
 - hit the **Start static export** button to trigger the automated deployment


{{% notice tip %}}
If it's your first time deploying to GitHub Pages, you'll need to ensure you're pushing to a repository/branch with at leat one commit. You can use the GitHub UI to quickly create a file in a branch.
{{% /notice %}}

### GitHub Pages configuration options explained

**Base URL**

Set this to the final domain your users will visit your site on. If you're just getting started you can set it to your GitHub Pages user/org's URL, ie https://mygitubuser.github.io


_More option usage being written now and expected up within the day_

_Need more help in the meantime, join our [Support Community](https://wp2static.com/community/)_



{{% notice tip %}}
Did you know, you don't need to save any of your credentials within the plugin if you are exporting via the UI (vs CRON/CLI). Just enter your credentials on the settings page and hit *Start static site export*. If you navigate away from the page, your credentials will not persist. You can also hit the *Reset to default settings* button to clear any settings you've saved for the plugin from your WordPress database.
{{% /notice %}}
