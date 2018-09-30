---
title: Deploying
pre: "<b>3. </b>"
weight: 15
---

Deploying is the part of the process which takes place once your site has been "exported".


{{<mermaid align="left">}}
graph LR;
	A[Crawl site] -->|exported archive| B(Process archive)
    B -->|processed archive| C(Deploy static representation of your site)
{{< /mermaid >}}
