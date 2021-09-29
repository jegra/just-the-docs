---
layout: default
title: Layout
parent: Utilities
---

# Layout Utilities
{: .no_toc }

## Table of contents
{: .no_toc .text-delta }

1. TOC
{:toc}

---

## Spacing

These spacers are available to use for margins and padding with responsive utility classes. Combine these prefixes with a screen size and spacing scale to use them responsively.

| Classname prefix | What it does                  |
|:-----------------|:------------------------------|
| `.m-`            | `margin`                      |
| `.mx-`           | `margin-left`, `margin-right` |
| `.my-`           | `margin top`, `margin bottom` |
| `.mt-`           | `margin-top`                  |
| `.mr-`           | `margin-right`                |
| `.mb-`           | `margin-bottom`               |
| `.ml-`           | `margin-left`                 |

| Classname prefix | What it does                    |
|:-----------------|:--------------------------------|
| `.p-`            | `padding`                       |
| `.px-`           | `padding-left`, `padding-right` |
| `.py-`           | `padding top`, `padding bottom` |
| `.pt-`           | `padding-top`                   |
| `.pr-`           | `padding-right`                 |
| `.pb-`           | `padding-bottom`                |
| `.pl-`           | `padding-left`                  |

Spacing values are based on a `1rem = 16px` spacing scale, broken down into these units:

| Spacer/suffix  | Size in rems  | Rem converted to px |
|:---------------|:--------------|:--------------------|
| `1`            | 0.25rem       | 4px                 |
| `2`            | 0.5rem        | 8px                 |
| `3`            | 0.75rem       | 12px                |
| `4`            | 1rem          | 16px                |
| `5`            | 1.5rem        | 24px                |
| `6`            | 2rem          | 32px                |
| `7`            | 2.5rem        | 40px                |
| `8`            | 3rem          | 48px                |
| `9`            | 3.5rem        | 56px                |
| `10`           | 4rem          | 64px                |
| `auto`         | auto          | auto                |

Use `mx-auto` to horizontally center elements.

#### Examples
{: .no_toc }

In Markdown, use the `{: }` wrapper to apply custom classes:

```markdown
This paragraph will have a margin bottom of 1rem/16px at large screens.
{: .mb-lg-4 }

This paragraph will have 2rem/32px of padding on the right and left at all screen sizes.
{: .px-6 }
```

## Horizontal Alignment

| Classname               | What it does                     |
|:------------------------|:---------------------------------|
| `.float-left`           | `float: left`                    |
| `.float-right`          | `float: right`                   |
| `.flex-justify-start`   | `justify-content: flex-start`    |
| `.flex-justify-end`     | `justify-content: flex-end`      |
| `.flex-justify-between` | `justify-content: space-between` |
| `.flex-justify-around`  | `justify-content: space-around`  |

_Note: any of the `flex-` classes must be used on a parent element that has `d-flex` applied to it._

## Vertical Alignment

| Classname              | What it does                    |
|:-----------------------|:--------------------------------|
| `.v-align-baseline`    | `vertical-align: baseline`      |
| `.v-align-bottom`      | `vertical-align: bottom`        |
| `.v-align-middle`      | `vertical-align: middle`        |
| `.v-align-text-bottom` | `vertical-align: text-bottom`   |
| `.v-align-text-top`    | `vertical-align: text-top`      |
| `.v-align-top`         | `vertical-align: top`           |

## Display

Display classes aid in adapting the layout of the elements on a page:

| Class             |                         |
|:------------------|:------------------------|
| `.d-block`        | `display: block`        |
| `.d-flex`         | `display: flex`         |
| `.d-inline`       | `display: inline`       |
| `.d-inline-block` | `display: inline-block` |
| `.d-none`         | `display: none`         |

Use these classes in conjunction with the responsive modifiers.

#### Examples
{: .no_toc }

In Markdown, use the `{: }` wrapper to apply custom classes:

```markdown
This button will be hidden until medium screen sizes:

[ A button ](#url)
{: .d-none .d-md-inline-block }

These headings will be `inline-block`:

### heading 3
{: .d-inline-block }

### heading 3
{: .d-inline-block }
```

## Basic Grid

When grid structures are needed, the provided grid utility classes -- in conjunction with some basic HTML wrapper elements -- can be used to build responsive grid layouts.

To create a grid, an outer `<div>` element is added to the page, containing a `.basic-grid` class assignment.  Additional classes may be added to specify the number of columns shown on desktop, and/or if a divider should be shown between stacked elements in the grid.

*Note: the default Basic Grid layout displays with 1 column on mobile, and 2 columns on desktop.  Class modifiers may be added to increase the number of columns.*

| Classname        | What it does          |
|:-----------------|:------------------------|
| `.basic-grid`    | when added to a parent element, creates a grid container |
| `.with-dividers` | when added to a '.basic-grid' element, adds dividers between stacked elements  |
| `.three-column`  | when added to a '.basic-grid' element, shows 3 columns on desktop |
| `.four-column`   | when added to a '.basic-grid' element, shows 4 columns on desktop |

#### Example
{: .no_toc }

Here is a sample Basic Grid layout, where content will be arranged in a 3 column responsive grid on desktop:

```html
<div class="basic-grid three-column">

<div markdown="1">
## Grid element heading
Lorem ipsum dolor sit amet, consectetur adipiscing elit. 
</div>
<div markdown="1">
## Grid element heading
Lorem ipsum dolor sit amet, consectetur adipiscing elit. 
</div>
<div markdown="1">
## Grid element heading
Lorem ipsum dolor sit amet, consectetur adipiscing elit. 
</div>

</div><!-- end grid -->
```

**⚠️Important:** in order to use markdown within the grid elements, the `markdown="1"` attribute must be added to the child elements in the grid. Also, to render out the markdown correctly, be sure there is no space/tab to the left of the content in each of the grid elements.

## Enhanced Grid

When more complex grid structures are needed, the 'row/col' grid utility classes may be used -- in conjunction with some basic HTML wrapper elements -- instead of the Basic Grid system.  

The Enhanced Grid system is based on a 12 column layout, where classes are used to indicate how many of the 12 columns should be filled by the child element at a particular breakpoint.  For example, `col-sm-6` means that at the `sm` breakpoint (and up), the element should fill 6 of the 12 'base' columns (ie should fill half of the space of the parent row).

| Classname (/prefix) | What it does          |
|:------------------  |:------------------------|
| `.row`              | when added to a parent element, creates a grid row        |
| `.col-xs-`          | when added to a child element, creates a column at the smallest screen widths        |
| `.col-sm-`          | specifies a column at the `sm` breakpoint       |
| `.col-md-`          | specifies a column at the `md` breakpoint |
| `.col-lg-`          | specifies a column at the `lg` breakpoint         |


#### Example
{: .no_toc }

Here is a sample grid layout, where each child element within the grid row will fill the full screen width at the smallest (`xs`) browser sizes (12 of 12 columns), and then will switch to half screen width (6 of 12 columns) when the 'small' (`sm`) screen breakpoint is hit:

```html
<div class="row">

<div class="col-xs-12 col-sm-6">
<!-- This content will take up 6/12 (or 1/2) of the container at the `sm` breakpoint -->
</div>
<div class="col-xs-12 col-sm-6">
<!-- This content will take up 6/12 (or 1/2) of the container at the `sm` breakpoint -->
</div>

</div><!-- end grid -->
```
**⚠️Important:** as with the Basic Grid configuration, if you would like to use markdown within the grid elements, a `markdown="1"` attribute must be added to the child elements in the grid. Also, to render out the markdown correctly, be sure there is no space/tab to the left of the content in each of the grid elements.

The grid system is based on the [Flexbox Grid](https://github.com/kristoferjoseph/flexboxgrid) project. More information, including details on alignment, offsets, and nesting, can be found [here](http://flexboxgrid.com/). 

## Image Cards

Pre-configured 'Image Cards' may be used to display a linkable image with text label. These can be combined with grid layouts to create a matrix of image links.

Image Cards make use of an include file, where properties of the card are passed in as attributes.

| Attribute        | What it's for                                 |
|:-----------------|:----------------------------------------------|
| `image`          | path to the image file                        |
| `link`           | (optional) specifies the url to link out to   |
| `label`          | text to display below the image               |

#### Examples
{: .no_toc }

Here is a sample Image Card include:

```html
{% raw %}{% include image-card.html 
    image="https://via.placeholder.com/500"
    link="http://example.com/"
    label="Label for our image"
%}{% endraw %}
```

And here is a sample of the Image Card include used within a Basic Grid:

```html
<div class="basic-grid three-column">

<div markdown="1">
{% raw %}{% include image-card.html 
    image="https://via.placeholder.com/500"
    link="http://example.com/"
    label="Label for our image"
%}{% endraw %}
</div>
<div markdown="1">
{% raw %}{% include image-card.html 
    image="https://via.placeholder.com/500"
    link="http://example.com/"
    label="Label for our image"
%}{% endraw %}
</div>
<div markdown="1">
{% raw %}{% include image-card.html 
    image="https://via.placeholder.com/500"
    link="http://example.com/"
    label="Label for our image"
%}{% endraw %}
</div>

</div><!-- end grid -->
```

#### Renders as:
{: .no_toc }

<div class="basic-grid three-column">

<div markdown="1">
{% include image-card.html 
    image="https://via.placeholder.com/500"
    link="http://example.com/"
    label="Label for our image"
%}
</div>
<div markdown="1">
{% include image-card.html 
    image="https://via.placeholder.com/500"
    link="http://example.com/"
    label="Label for our image"
%}
</div>
<div markdown="1">
{% include image-card.html 
    image="https://via.placeholder.com/500"
    link="http://example.com/"
    label="Label for our image"
%}
</div>

</div><!-- end grid -->