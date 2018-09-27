# Documentation website for [WP Static Site Generator](https://wp2static.com)

Herein lies the content for the documentation site, which is viewable at [https://wp-static-site-generator-documentation.netlify.com](https://wp-static-site-generator-documentation.netlify.com)

## Contributing

Contributions are welcome and encouraged - were you trying to follow along with the documentation and discovered something confusing/incorrect/missing?

Simply 

 - fork this repository into your own GitHub account
 - make the changes
 - submit a pull request. 
 
 As soon as it's merged, it will rebuild the site on the amazing [Netlify](https://netlify.com) platform. Your changes will then be publicly viewable shortly after.

If you're making a lot of contributions to the documentation, we'll add you as a **contributor**, so you can bypass the pull request process for quicker publishing.

## Working locally

 - Install [Hugo](https://gohugo.io/getting-started/installing)
 - `git clone git@github.com:leonstafford/wp-static-site-generator-documentation.git`
 - `cd wp-static-site-generator-documentation`
 - `hugo server --disableFastRender`

The local development server should then be viewable at [http://localhost:1313](http://localhost:1313/) 

## Site structure

The site's content primarily lives in the `./content/` directory. 

The pages you see in the site's sidebar follow this structure, ie:

```
├── basics
│   ├── configuration
│   ├── _index.en.md
│   ├── _index.fr.md
│   ├── installation
│   ├── style-customization
│   └── what-is-static
├── cont
│   └── markdown.en.md
├── getting-started
│   ├── configuration
│   ├── _index.en.md
│   ├── _index.fr.md
│   ├── installation
│   ├── requirements
│   └── style-customization
├── _index.en.md
├── posts
│   └── getting-started.md
└── shortcodes
    ├── _index.en.md
    ├── _index.fr.md
    ├── mermaid.en.md
    ├── mermaid.fr.md
    ├── notice.en.md
    ├── notice.fr.md
    ├── siteparam.en.md
    └── ... etc

```
