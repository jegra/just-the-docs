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

## Grid

When grid structures are needed, the provided grid utility classes -- in conjunction with some basic HTML wrapper elements -- can be used to build responsive grid layouts.  

Grids are based on a 12 column layout, where classes are used to indicate how many of the 12 columns should be filled by the child element at a particular breakpoint.  For example, `col-sm-6` means that at the `sm` breakpoint (and up), the element should fill 6 of the 12 'base' columns (ie should fill half of the space of the parent row).

| Classname (/prefix) | What it does          |
|:------------------  |:------------------------|
| `.row`              | when added to a parent element, creates a grid row        |
| `.col-xs-`          | when added to a child element, creates a column at the smallest screen widths        |
| `.col-sm-`          | specifies a column at the `sm` breakpoint       |
| `.col-md-`          | specifies a column at the `md` breakpoint |
| `.col-lg-`          | specifies a column at the `lg` breakpoint         |


#### Examples
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
</div>
```

The grid system is based on the [Flexbox Grid](https://github.com/kristoferjoseph/flexboxgrid) project. More information, including details on alignment, offsets, and nesting, can be found [here](http://flexboxgrid.com/). 