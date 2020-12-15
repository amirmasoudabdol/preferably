# preferably <img src="man/figures/logo.png" width="20%" align="right"/>

preferably is a pkgdown template. preferably uses two bootstrap themes, [Darkly](https://bootswatch.com/darkly/) and [Flatly](https://bootswatch.com/flatly/) and utilizes [prefers-color-scheme](`https://developer.mozilla.org/en-US/docs/Web/CSS/@media/prefers-color-scheme`) to serve either of the themes based on users system's color theme.


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