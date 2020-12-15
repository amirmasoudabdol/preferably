# preferably <img src="man/figures/logo.png" width="20%" align="right"/>

preferably is a pkgdown template. preferably uses two bootstrap themes, [Darkly](https://bootswatch.com/darkly/) and [Flatly](https://bootswatch.com/flatly/) and utilizes the [prefers-color-scheme](`https://developer.mozilla.org/en-US/docs/Web/CSS/@media/prefers-color-scheme`) variable to serve either of the themes based on users system's color theme.

## Introduction

As modern OSes are offering system-wide dark mode, browsers are providing mechanism to detect system-wide color scheme and react to it. Websites can take advantages of these mechanism and deliver a customized page to their visitors that matches their preferences. 

Preferably brings these advancement and customizations to pkgdown by delivering a light theme when users setting is in light mode, and delivering dark theme when users is adapting a dark mode. Moreover, [if supported](https://support.apple.com/en-us/HT208976), a light theme can be delivered during the day, and a dark theme during the night. 

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

In addition of pkgdown customizations, Preferably offers a few more options as listed here.  

### Custom Analytic

Preferably allows for adding a custom tracker (in addition to `ganalytics`) to your website via the `customanalytic` option.

```YAML
template:
  package: preferably
  params:
    customanalytic:
      domain: example.com
      src: https://example.com/tracker.js
  default_assets: false
```

Setting these command will generate the following line in the HTML:

```html
<script async defer data-domain="example.com" src="https://example.com/tracker.js"></script>
```

In case this setting doesn’t satisfy your need or you have a better idea on how to implement this, please reach out on [GitHub](https://github.com/amirmasoudabdol/preferably/issues/)

### Light/Dark Switch

To be implemented