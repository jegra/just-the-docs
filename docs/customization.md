---
layout: default
title: Customization
nav_order: 6
---

# Customization
{: .no_toc }

## Table of contents
{: .no_toc .text-delta }

1. TOC
{:toc}

---

## Color schemes
{: .d-inline-block }

New
{: .label .label-green }

Just the Docs supports four color schemes: light (default), blue, bold, and dark.

To enable a color scheme, set the `color_scheme` parameter in your site's `_config.yml` file:

#### Example
{: .no_toc }

```yaml
# Color scheme supports "light" (default), "blue", "bold", and "dark"
color_scheme: blue
```
<button class="btn btn-primary js-set-color-scheme" data-mode="light">Light Scheme (default)</button>
<button class="btn btn-primary js-set-color-scheme" data-mode="blue">Blue Scheme</button>
<button class="btn btn-primary js-set-color-scheme" data-mode="bold">Bold Scheme</button>
<button class="btn btn-primary js-set-color-scheme" data-mode="dark">Dark Scheme</button>

<script>
const colorSchemeBtns = document.querySelectorAll('.js-set-color-scheme');

colorSchemeBtns.forEach((btn) => {
  jtd.addEvent(btn, 'click', function(){
    const theme = btn.dataset.mode;
    jtd.setTheme(theme);
  });
});
</script>

## Custom schemes

### Define a custom scheme

You can add custom schemes.
If you want to add a scheme named `foo` (can be any name) just add a file `_sass/color_schemes/foo.scss` (replace `foo` by your scheme name) 
where you override theme variables to change colors, fonts, spacing, etc.

Available variables are listed in the [_variables.scss](https://github.com/labsyspharm/just-the-docs-lsp/blob/main/_sass/support/_variables.scss) file.

For example, to change the link color from the green default to blue, include the following inside your scheme file:

#### Example
{: .no_toc }

```scss
$link-color: $blue-000;
```

_Note:_ Editing the variables directly in `_sass/support/variables.scss` is not recommended and can cause other dependencies to fail.
Please use scheme files.

### Use a custom scheme

To use the custom color scheme, only set the `color_scheme` parameter in your site's `_config.yml` file:
```yaml
color_scheme: foo
```

### Switchable custom scheme

If you want to be able to change the scheme dynamically, for example via javascript, just add a file `assets/css/just-the-docs-foo.scss` (replace `foo` by your scheme name)
with the following content:`

{% raw %}
    ---
    ---
    {% include css/just-the-docs.scss.liquid color_scheme="foo" %}
{% endraw %}

This allows you to switch the scheme via the following javascript.

```js
jtd.setTheme('foo');
```

## Override and completely custom styles

For styles that aren't defined as variables, you may want to modify specific CSS classes.
Additionally, you may want to add completely custom CSS specific to your content.
To do this, put your styles in the file `_sass/custom/custom.scss`.
This will allow for all overrides to be kept in a single file, and for any upstream changes to still be applied.

For example, if you'd like to add your own styles for printing a page, you could add the following styles.

#### Example
{: .no_toc }

```scss
// Print-only styles.
@media print {
  .side-bar, .page-header { display: none; }
  .main-content { max-width: auto; margin: 1em;}
}
```
