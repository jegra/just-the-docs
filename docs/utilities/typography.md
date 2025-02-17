---
layout: default
title: Typography
parent: Utilities
---

# Typography Utilities
{: .no_toc }

## Table of contents
{: .no_toc .text-delta }

1. TOC
{:toc}

---

## Font size

Use the `.fs-1` - `.fs-10` to set an explicit font-size.

| Class   | Small screen size `font-size`  | Large screen size `font-size` |
|:--------|:-------------------------------|:------------------------------|
| `.fs-1` | 9px                            | 10px                          |
| `.fs-2` | 12px                           | 14px                          |
| `.fs-3` | 14px                           | 16px                          |
| `.fs-4` | 16px                           | 18px                          |
| `.fs-5` | 18px                           | 20px                          |
| `.fs-6` | 20px                           | 22px                          |
| `.fs-7` | 22px                           | 24px                          |
| `.fs-8` | 24px                           | 30px                          |
| `.fs-9` | 30px                           | 32px                          |
| `.fs-10`| 38px                           | 44px                          |

<div class="code-example" markdown="1">
Font size 1
{: .fs-1 }
Font size 2
{: .fs-2 }
Font size 3
{: .fs-3 }
Font size 4
{: .fs-4 }
Font size 5
{: .fs-5 }
Font size 6
{: .fs-6 }
Font size 7
{: .fs-7 }
Font size 8
{: .fs-8 }
Font size 9
{: .fs-9 }
Font size 10
{: .fs-10 }
</div>
```markdown
In Markdown, use the `{: }` wrapper to apply custom classes:

Font size 1
{: .fs-1 }
Font size 2
{: .fs-2 }
Font size 3
{: .fs-3 }
Font size 4
{: .fs-4 }
Font size 5
{: .fs-5 }
Font size 6
{: .fs-6 }
Font size 7
{: .fs-7 }
Font size 8
{: .fs-8 }
Font size 9
{: .fs-9 }
Font size 10
{: .fs-10 }
```

### Global font size adjustments

There are a series of variables that can be set in the theme's [color scheme file]({% link docs/customization.md %}) that allow for the global override of font sizes for specific elements.  Using the `fs-x` system of size specifications (outlined above), the elements will size dynamically, based on the viewing device's browser width.

| Variable name | Default size assignment |
|:------------------------|:--------------|
| `$body-font-size`       | `fs-4`        | 
| `$h1-font-size`         | `fs-9`        | 
| `$h2-font-size`         | `fs-7`        | 
| `$h3-font-size`         | `fs-4`        | 
| `$h4-font-size`         | `fs-2`        | 
| `$h5-font-size`         | `fs-3`        | 
| `$h6-font-size`         | `fs-2`        | 
| `$text-small-font-size` | `fs-2`        | 

```scss
In the color scheme file, overrides would be assigned like so:

$body-font-size: fs-3;
$h2-font-size: fs-8;
```


## Font weight

Use the `.fw-300` - `.fw-700` to set an explicit font-weight.

<div class="code-example" markdown="1">
Font weight 300
{: .fw-300 }
Font weight 400
{: .fw-400 }
Font weight 500
{: .fw-500 }
Font weight 700
{: .fw-700 }
</div>
```markdown
In Markdown, use the `{: }` wrapper to apply custom classes:

Font weight 300
{: .fw-300 }
Font weight 400
{: .fw-400 }
Font weight 500
{: .fw-500 }
Font weight 700
{: .fw-700 }
```

## Line height

Use the `lh-` classes to explicitly apply line height to text.

| Class         | `line-height` value  | Notes                         |
|:--------------|:---------------------|:------------------------------|
| `.lh-0`       | 0                    |                               |
| `.lh-tight`   | 1.1                  | Default for headings          |
| `.lh-default` | 1.4                  | Default for body (paragraphs) |

<div class="code-example" markdown="1">
No Line height
No Line height
{: .lh-0 }

Tight line height
Tight line height
{: .lh-tight }

Default line height
Default line height
{: .fh-default }
</div>
```markdown
In Markdown, use the `{: }` wrapper to apply custom classes:

No Line height
No Line height
{: .lh-0 }

Tight line height
Tight line height
{: .lh-tight }

Default line height
Default line height
{: .fh-default }
```

## Text justification

By default text is justified left. Use these `text-` classes to override settings:

| Class          | What it does         |
|:---------------|:---------------------|
| `.text-left`   | `text-align: left`   |
| `.text-right`  | `text-align: right`  |
| `.text-center` | `text-align: center` |
