# preferably 0.4.1

## Changes

- Fixed the issue where the footer was not adhereing to the dark mode. Reported by @bryce-carson, https://github.com/amirmasoudabdol/preferably/issues/12.
- Modified the `.page-header` and added a bit of margin to the header itself. Thanks @zero323!
- Updated for `{pkgdown}` 2.0.6.

# preferably 0.4

## New

- Support for `{pkgdown}` 2.0, and [Bootstrap 5](https://pkgdown.r-lib.org/articles/customise.html?q=boos#getting-started)


# preferably 0.3.2

## Changes

- Fixed a minor issue with the footer, https://github.com/amirmasoudabdol/preferably/issues/8#issuecomment-957228703

## Known Issues

- If you don't see the footer showing up, you need to specify it explicitly, see [here](https://pkgdown.r-lib.org/articles/customise.html?q=footer#footer).

# preferably 0.3.1

## Changes

- Changed the color of hyperlink in the light mode from `#18BC9B` to `#11866F` which has a better contrast ratio with the light background. Thanks @EllaKaye!

# preferably 0.3.0

## New

- In the manual light/dark mode, preferably now uses localStorage to remember user's preference.

## Changes

- Automatic and manual switching cannot be activated at the same time anymore.
	- It is almost impossible to deliver a seamless experience without involving the server-side. So, you need to choose whether you like to give your users a manual toggle, or let your website adapts to their system preference.

# preferably 0.2.0

## New

- Ability to add a custom analytic script using `canalytics` parameter.
- Ability to add a light/dark toggle button using `toggle` parameter.

## Improved

- Reduced the overall size of the package

## preferably 0.1.0

- This is the initial release of the `preferably` template!
