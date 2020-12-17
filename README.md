<!-- badges: start -->
[![Travis build status](https://travis-ci.com/amirmasoudabdol/preferably.svg?branch=main)](https://travis-ci.com/amirmasoudabdol/preferably)
<!-- badges: end -->

# preferably <img src="man/figures/logo.png" width="20%" align="right"/>

preferably is an **accessible** template for [pkgdown](https://pkgdown.r-lib.org/). It uses two bootstrap themes, [Flatly](https://bootswatch.com/flatly/) and [Darkly](https://bootswatch.com/darkly/) and utilizes the [`prefers-color-scheme`](https://developer.mozilla.org/en-US/docs/Web/CSS/@media/prefers-color-scheme) CSS variable to automatically serve either of the two based on user’s operating system setting, or allowing them to manually toggle between them.

Besides offering light and dark mode, I have spent some time to make the overall reading experience of reading documents just a bit nicer, by using richer fonts, adopting a better color scheme for codes, etc. 

![](man/figures/comparison.png)

## Installation

```R
install.packages("devtools"); library(devtools)

devtools::install_github("amirmasoudabdol/preferably")
```

## Usage

```YAML
template:
  package: preferably
  default_assets: false
```

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
  default_assets: false
```

Setting these command will generate the following line in the HTML:

```html
<script async defer data-domain="example.com" src="https://example.com/tracker.js"></script>
```

In case this setting does not satisfy your need or you have a better idea on how to implement this, please reach out on [GitHub](https://github.com/amirmasoudabdol/preferably/issues/)

### Light/Dark Switch

In addition to the automatic color scheme switching, you can add a switch to manually toggle between light and dark themes. This can be done by setting the `toggle` option to `manual`.

```YAML
  package: preferably
  params:
    toggle: manual
```

In order to remove the toggle button, remove the `toggle` parameters entirely.
