---
date: 2016-04-09T16:50:16+02:00
title: Troubleshooting
pre: "<b>4. </b>"
weight: 20
---

> When you have eliminated all which is impossible, then whatever remains, however improbable, must be the truth.
>
>  <cite>Sir Arthur Ignatius Conan Doyle</cite>

Encountered an issue during your journey from WordPress to static site publishing?

There are many variables involved in software, computing and life itself. Let's work methodically to isolate what the issue is. This often involves confirmation that several things are **not** the problem. 

Once we have isolated the issue, there may be a documented solution, you may be able to figure one out yourself (in this case, please share it with the community, to save others the same pain!) or it may be an issue requiring a fix to the code in the plugin.

### Where is the problem occuring?

Click on the area the issue seems to be occurring, for solutions to common issues in that area:

{{<mermaid align="center">}}
graph TD
    downloading[fa:fa-download Downloading] --> installation[Installation] 
    installation --> activation[Activation] 
    activation[Activation] --> optingin[Opting in]
    updating[Updating] --> optingin[Opting in] 
    optingin[fa:fa-check Opting in] --> viewsettings[fa:fa-eye View settings]
    viewsettings[View settings] --> startexport[fa:fa-flag-checkered Start export]
    startexport[Start export] --> checksite[fa:fa-search Check site]
    viewsettings[View settings] --> savesettings[fa:fa-save Save settings]
    viewsettings[View settings] --> resettodefaults[fa:fa-reset Reset to default settings]
    viewsettings[View settings] --> choosedeployoption[Choose deployment option]
    choosedeployoption[Choose deployment option] --> testdeploy[Test deploy]
    choosedeployoption[Choose deployment option] --> github[fa:fa-github GitHub]
    choosedeployoption[Choose deployment option] --> netlify[Netlify]
    choosedeployoption[Choose deployment option] --> s3[S3]
    choosedeployoption[Choose deployment option] --> ftp[FTP]
    choosedeployoption[Choose deployment option] --> bunnycdn[BunnyCDN]
    choosedeployoption[Choose deployment option] --> dropbox[fa:fa-dropbox Dropbox]
    click downloading "/en/troubleshooting/downloading/"
    click checksite "/en/troubleshooting/start-export/check-site/"
    click ftp "/en/troubleshooting/view-settings/choose-deployment-option/ftp/"
    click activation "/en/troubleshooting/activation/"
{{< /mermaid >}}

Still unable to locate the issue? Join our [support community](https://wp2static.com/community/) for more assistance.
