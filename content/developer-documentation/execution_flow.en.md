---
title : "Execution flow"
description : "The flow of information as we export and deploy a static version of our WP site"
---

The flow of information as we export and deploy a static version of our WP site

## Basic deployment example

{{<mermaid align="left">}}
graph LR;
	A[Detect WP site configuration] -->|Set options| B(Crawl the site)
    B --> C{Deployment}
    C --> D[GitHub Pages]
    C --> E[Amazon S3]
    C --> F[Netlify]
    C --> G[BunyCDN]
    C --> H[FTP Server]
    C --> I[Dropbox]
{{< /mermaid >}}

## Sequence example

{{<mermaid>}}
sequenceDiagram
    participant Alice
    participant Bob
    Alice->>John: Hello John, how are you?
    loop Healthcheck
        John->John: Fight against hypochondria
    end
    Note right of John: Rational thoughts <br/>prevail...
    John-->Alice: Great!
    John->Bob: How about you?
    Bob-->John: Jolly good!
{{< /mermaid >}}




