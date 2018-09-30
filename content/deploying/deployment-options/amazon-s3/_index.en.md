---
title: Amazon S3
weight: 10
disableToc: true
---

### Pros

 - Low-cost
 - Free tier available
 - Custom domain support
 - Easy integration with CloudFront for improved performance

### Costs

From [$0.023/GB](https://aws.amazon.com/s3/pricing/)

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


{{% notice note %}}
TIP: For easier deployments via the ZIP (or even the "Test deploy" method), consider using an S3 backed filesystem to automatically sync a directory to an S3 bucket!
{{% /notice %}}

#### Auto deploy with the Pro version 

 - select the S3 deployment method within the plugin's settings

![S3 deployment option](/images/ui/s3_deployment_option.png)

 - configure your [S3 related deployment options](#s3-configuration-options-explained)
 - optionally set any other [configuration](/configuration) options for the crawling, processing or deployment phases 
 - hit the **Start static export** button to trigger the automated deployment


{{% notice note %}}
TIP: If it's your first time deploying to S3, it may help to do a quick test by manually uploading an index.html file to your S3 bucket's root and ensuring you can access it at your intended domain. If hat works, then you should be ready to deploy your whole WP site there
{{% /notice %}}

### S3 configuration options explained

**Base URL**

For an S3 hosted website, you have a few options which will influence what you put in this field.


 - _Direct bucket hosting_ If you want to serve your site directly from S3, you'll want the Endpoint as shown in your AWS console, when you go to your bucket > properties > Static website hosting, ie for a bucket named 'statictestfrankfurt', hosted in the eu-central-1 region, it will be: http://statictestfrankfurt.s3-website.eu-central-1.amazonaws.com

 - _Bucket with a custom domain_ If you've setup a custom domain to use with your S3 bucket hosted, use that domain. In this case, your bucket name should already be the same as the domain, ie statictest.mydomain.org, with an A record alias entry in Route53 or your DNS provider to s3-website-ap-southeast-1.amazonaws.com. So, we would use http://statictest.mydomain.org/ as the Base Url in this case.

 - _S3 hosted website cached with CloudFront_ If you've setup CloudFront to speed up your S3 hosted static site, then entering your CloudFront Distribution ID here will send a cache invalidation request after all the files have been deployed to S3. It will use the same AWS credentials as S3, so ensure that IAM user in AWS has the correct permissions for both S3 and CloudFront. You could set the BaseURL to the CloudFront address, ie http://d3fvx8eaa0pipc.cloudfront.net/, but more than likely, you have another domain you want to use for the website, so set the Base Url to that, ie https://mywebsite.com.

**Access Key ID**

Your S3 user will need permissions to put objects into the bucket. Check that the user whose Key you are using has the correct permissions for S3. You may attach the 'AmazonS3FullAccess' to the user or give more fine grained permissions control via [AWS's IAM](https://aws.amazon.com/iam/).


