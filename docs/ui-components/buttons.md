---
layout: default
title: Buttons
parent: UI Components
nav_order: 2
---

# Buttons
{: .no_toc }

## Table of contents
{: .no_toc .text-delta }

1. TOC
{:toc}

---

## Basic button styles

### Links that look like buttons

<div class="code-example" markdown="1">
[Link button](http://example.com/){: .btn }
[Link button](http://example.com/){: .btn .btn-primary }

[Link button](http://example.com/){: .btn .btn-blue }
[Link button](http://example.com/){: .btn .btn-green }

[Link button](http://example.com/){: .btn .btn-outline }

[Link button](http://example.com/){: .btn .btn-outline .btn-arrow }
</div>
```markdown
[Link button](http://example.com/){: .btn }
[Link button](http://example.com/){: .btn .btn-primary }

[Link button](http://example.com/){: .btn .btn-blue }
[Link button](http://example.com/){: .btn .btn-green }

[Link button](http://example.com/){: .btn .btn-outline }

[Link button](http://example.com/){: .btn .btn-outline .btn-arrow }
```

### Button element

GitHub Flavored Markdown does not support the `button` element, so you'll have to use inline HTML for this:

<div class="code-example">
<button type="button" name="button" class="btn">Button element</button>
</div>
```html
<button type="button" name="button" class="btn">Button element</button>
```

---

## ADDITIONAL MODIFICATIONS

### Button size

Use the `btn-large` class to increase the size of the button:

<div class="code-example" markdown="1">
[Large button](http://example.com/){: .btn .btn-large }

[Large button](http://example.com/){: .btn .btn-large .btn-arrow }

[Large button](http://example.com/){: .btn .btn-large .btn-arrow .btn-outline }
</div>
```markdown
[Large button](http://example.com/){: .btn .btn-large }

[Large button](http://example.com/){: .btn .btn-large .btn-arrow }

[Large button](http://example.com/){: .btn .btn-large .btn-arrow .btn-outline }
```

### Spacing between buttons

Use the [margin utility classes]({{ site.baseurl }}{% link docs/utilities/layout.md %}#spacing) to add spacing between two buttons in the same block.

<div class="code-example" markdown="1">
[Button with space](http://example.com/){: .btn .btn-purple .mr-2 }
[Button ](http://example.com/){: .btn .btn-blue .mr-2 }

[Button with more space](http://example.com/){: .btn .btn-green .mr-4 }
[Button ](http://example.com/){: .btn .btn-blue }
</div>
```markdown
[Button with space](http://example.com/){: .btn .btn-purple .mr-2 }
[Button ](http://example.com/){: .btn .btn-blue }

[Button with more space](http://example.com/){: .btn .btn-green .mr-4 }
[Button ](http://example.com/){: .btn .btn-blue }
```
