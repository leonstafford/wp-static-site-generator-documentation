---
title: FTP deployment option
weight: 60
---

### Troubleshooting 

Usually, FTP issues will be down to:

- incorrect login details
- passive/active mode
- remote path

Suggest double/triple checking your credentials with FileZilla or such FTP client. Make sure that not only can you connect, but that you can create files and directories in the remote path that you're intending to use

The 5.8 version of the plugin doesn't do a great job of surfacing any FTP related errors, so you may need to look at your server's PHP error logs to see exact errors being returned
Alternatively, you can use the ZIP download method and manually upload if unable to resolve the FTP deployment
