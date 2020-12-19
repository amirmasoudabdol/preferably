# preferably <img src="man/figures/logo.png" width="120" align="right"/>

preferably is an **accessible** template for [pkgdown](https://pkgdown.r-lib.org/). It uses a [light](https://bootswatch.com/flatly/) and a [dark](https://bootswatch.com/darkly/) theme and utilizes the [`prefers-color-scheme`](https://developer.mozilla.org/en-US/docs/Web/CSS/@media/prefers-color-scheme) CSS variable to *automatically* serve either of the two based on user’s operating system setting, or allowing them to manually toggle between them.

Besides offering light and dark mode, I have spent some time making the overall reading experience of pkgdown documentations just a bit nicer, by using richer fonts, adopting a better color scheme for codes, etc. 

![](man/figures/comparison.png)

## Installation

```R
install.packages("devtools"); library(devtools)

devtools::install_github("amirmasoudabdol/preferably")
```

## Usage

After the successful installation, you need to prepare your `_pkgdown.yml` config file:

```YAML
template:
  package: preferably
```

> ⚠️ *Keep in mind that you should NOT use `default_assets: false` when you change the default template. 'preferably' relies on some of the 'pkgdown' assets and templates.*

## Customization

In addition of pkgdown customization, Preferably offers a few more options as listed here.  

### Custom Analytic

Preferably allows for adding a custom analytics (in addition to `ganalytics`) to your website via the `canalytic` option.

```YAML
template:
  package: preferably
  params:
    canalytic:
      domain: example.com
      src: https://example.com/tracker.js
```

Setting these command will generate the following line in the HTML:

```html
<script async defer data-domain="example.com" src="https://example.com/tracker.js"></script>
```

In case this setting does not satisfy your need or you have a better idea on how to implement this, please reach out on [GitHub](https://github.com/amirmasoudabdol/preferably/issues/).

### Light/Dark Switch

In addition to the automatic color scheme switching, you can add a switch to the menu bar, e.g, <span class="fas fa-adjust fa"></span>, to allow for manual selection between light and dark themes. This can be done by setting the `toggle` option to `manual`.

```YAML
template:
  package: preferably
  params:
    toggle: manual
```

In order to remove the toggle button, remove the `toggle` parameters entirely.