<!-- badges: start -->
[![Travis build status](https://travis-ci.com/amirmasoudabdol/preferably.svg?branch=main)](https://travis-ci.com/amirmasoudabdol/preferably)
<!-- badges: end -->

# preferably <img src="man/figures/logo.png" width="20%" align="right"/>

`preferably` is a [pkgdown](https://pkgdown.r-lib.org/) template. `preferably` uses two bootstrap themes, [Flatly](https://bootswatch.com/flatly/) and [Darkly](https://bootswatch.com/darkly/) and utilizes the [`prefers-color-scheme`](https://developer.mozilla.org/en-US/docs/Web/CSS/@media/prefers-color-scheme) variable to serve either of the themes based on user’s operating system setting.

![](man/figures/comparison.png)

## Introduction

As most modern operation systems are offering system-wide dark mode, internet browsers are providing mechanism to detect user's system-wide color scheme. Therefore, it is possible for a website to advantages of these mechanism and automatically deliver a customized version of the website that matches user's operating system preference. 

`preferably` brings these advancement and customization to [pkgdown](https://pkgdown.r-lib.org/) by delivering a light theme when user's setting is set to *light mode*, and delivering dark theme when it is set to *dark mode*.

On [macOS](https://support.apple.com/en-us/HT208976), if automatic appearance is selected, a light theme will be delivered during the day time, and automatically changes to dark theme during the night time, and vice versa.

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
