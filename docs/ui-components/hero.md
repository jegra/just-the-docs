---
layout: default
title: Hero
parent: UI Components
nav_order: 7
---

# Hero

Hero blocks can be added to any page by specifying values for it in the page's front matter.  Note that if a `hero_background` image is defined in the site's `_config.yml` file, it will be used as the background for the hero element.

```yaml
# Hero heading and body text values
hero_heading: "Focus on writing good documentation"
hero_body: "Just the Docs gives your documentation a jumpstart
with a responsive Jekyll theme that is easily customizable and 
hosted on GitHub Pages."

# Call to action (CTA) buttons to be displayed within the hero area.
# 'label', 'link', and 'target' values can be specified for each
hero_ctas:
  - label: "Get started now"
    link: "#getting-started"
  - label: "View it on GitHub"
    link: "https://github.com/labsyspharm/just-the-docs-lsp"
    target: "_blank"
```