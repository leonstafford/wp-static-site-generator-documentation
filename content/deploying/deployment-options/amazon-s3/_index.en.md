---
title: Amazon S3
weight: 10
description: Low-cost, Free tier available, Custom domain support, Easy integration with CloudFront for improved performance
disableToc: true
---

### Pros

 - Low-cost
 - Free tier available
 - Custom domain support
 - Easy integration with CloudFront for improved performance

### Costs

From [$0.023/GB](https://aws.amazon.com/s3/pricing/) or you may be eligible for use it for free, within their [Free Tier](https://aws.amazon.com/free/)

### Official static web hosting guide

[Hosting a Static Website on Amazon S3](https://docs.aws.amazon.com/AmazonS3/latest/dev/WebsiteHosting.html)

### Deploying to S3 with WP Static Site Generator

 - [Manual deploy](#manual-deploy-with-the-free-version) Free version
 - [Auto deploy](#auto-deploy-with-the-pro-version) Pro version

#### Manual deploy with the free version

 - select the ZIP deployment method within the plugin's settings
 - set your Base URL to the final domain your users will visit your webite on
 - optionally set any other [configuration](/configuration) options for the crawling, processing or deployment phases 
 - generate your static site and download your resulting ZIP file
 - manually deploy the generated files and folders to your S3 bucket


{{% notice tip %}}
For easier deployments via the ZIP (or even the "Test deploy" method), consider using an S3 backed filesystem to automatically sync a directory to an S3 bucket!
{{% /notice %}}

#### Auto deploy with the Pro version 

 - select the S3 deployment method within the plugin's settings

![S3 deployment option](/images/ui/s3_deployment_option.png)

 - configure your [S3 related deployment options](#s3-configuration-options-explained)
 - optionally set any other [configuration](/configuration) options for the crawling, processing or deployment phases 
 - hit the **Start static export** button to trigger the automated deployment


{{% notice tip %}}
If it's your first time deploying to S3, it may help to do a quick test by manually uploading an index.html file to your S3 bucket's root and ensuring you can access it at your intended domain. If hat works, then you should be ready to deploy your whole WP site there
{{% /notice %}}

### S3 configuration options explained

**Base URL**

For an S3 hosted website, you have a few options which will influence what you put in this field.


 - _Direct bucket hosting_ If you want to serve your site directly from S3, you'll want the Endpoint as shown in your AWS console, when you go to your bucket > properties > Static website hosting, ie for a bucket named 'statictestfrankfurt', hosted in the eu-central-1 region, it will be: http://statictestfrankfurt.s3-website.eu-central-1.amazonaws.com

 - _Bucket with a custom domain_ If you've setup a custom domain to use with your S3 bucket hosted, use that domain. In this case, your bucket name should already be the same as the domain, ie statictest.mydomain.org, with an A record alias entry in Route53 or your DNS provider to s3-website-ap-southeast-1.amazonaws.com. So, we would use http://statictest.mydomain.org/ as the Base Url in this case.

 - _S3 hosted website cached with CloudFront_ If you've setup CloudFront to speed up your S3 hosted static site, then entering your CloudFront Distribution ID here will send a cache invalidation request after all the files have been deployed to S3. It will use the same AWS credentials as S3, so ensure that IAM user in AWS has the correct permissions for both S3 and CloudFront. You could set the BaseURL to the CloudFront address, ie http://d3fvx8eaa0pipc.cloudfront.net/, but more than likely, you have another domain you want to use for the website, so set the Base Url to that, ie https://mywebsite.com.

**Access Key ID**

Your S3 user will need permissions to put objects into the bucket. Check that the user whose Key you are using has the correct permissions for S3. You may attach the 'AmazonS3FullAccess' to the user or give more fine grained permissions control via [AWS's IAM](https://aws.amazon.com/iam/).

**Secret Access Key**

The other half of the authentication. Combined with the Access Key ID, this allows the plugin to authenticate with AWS when making requests.

**Region**

This must be set to the same region that your S3 bucket was created in. 

**Bucket**

Your bucket name as it appears in your [AWS Console for S3](https://s3.console.aws.amazon.com/s3/home).

**Subdirectory**

In case you want to put your site in a sub directory of a bucket, this will deploy all the static website files into the folder name you specify here.

**CloudFront Cache Invalidation**

If using CloudFront in your S3 static website setup, enter the CloudFront Distribution ID here and it will create an invalidation request for all files at the end of the deployment process. The invalidation usually happens within a few minutes. You can check any pending invalidations in your [AWS Console's CloudFront page](https://console.aws.amazon.com/cloudfront/home). You AWS user will need to have the CloudFrontFullAccess permissions or a more controlled policy, that includes the ability to send CloudFront invalidation requests.

{{% notice tip %}}
Did you know, you don't need to save any of your credentials within the plugin if you are exporting via the UI (vs CRON/CLI). Just enter your credentials on the settings page and hit *Start static site export*. If you navigate away from the page, your credentials will not persist. You can also hit the *Reset to default settings* button to clear any settings you've saved for the plugin from your WordPress database.
{{% /notice %}}
