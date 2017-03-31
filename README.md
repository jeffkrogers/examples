# Reflect Examples

**ReflectDocs**: https://reflect.io/docs/

**Note**: To test and manipulate this examples set please follow the guide below. To download themes for your personal application, please visit https://github.com/reflect/examples/blob/master/apps/themes/

## Prerequisites

- node.js (https://nodejs.org/en/)
- gulp (`npm install gulp`)

## Installation

Download the dependencies using `npm install`, and create the build directory and launch a local server with `gulp`. That's it!

A new tab should open in your browser directed at localhost:3000, or you can navigate there manually. If you decide to manipulate content in this repo--to swap in your personal view IDs for example--gulp will build and load your changes automatically.

## Custom themes

We are excited announce that custom theming will be made available in the coming months. In the meantime, this repo provides several variants of our default theme for you to clone as you please.

------

## Internal use

**Rules for new examples**
1. Must be 3 components or less, all full width
2. View title and component titles must be short enough to fit on iPhone 5. Toggle device toolbar on chrome to double check.
3. Must be sensical without legend items or controls (these are hidden on mobile -- tooltips are accessible on mobile).

**How to add new example**
1. Clone the `new-feature` folder in templates into `apps`. Rename a la `custom-colors`.
  - `view-name.html` needs view logic and custom controls. Annotate well. Rename a la `video-games.html`.
  - `view-name.png` should be replaced with a full-size screenshot of view. Rename a la `video-games.png`.
2. Add new example object to `examples.json`. Follow the form found in `sample-app.json`.
  - Double check that the lengths of description and example goals fit nicely across all sizes
3. If the example makes use of a new feature, follow the instructions in `sample-app.json` to add docs url and feature color.

**How to create new theme**
1. Clone `sample-theme.scss` into `apps/themes`.
2. Generally, you should only need to update the top-most variable-set titled `custom variables` and then uncomment the palette logic you want. (Be sure to comment out the others.)
3. Change the theme property of an app in `examples.json` to apply theme.  

**Notes**
- The `css` and `minified-css` folders in `app/themes` are generated by gulp. They are cleaned when `gulp` or `gulp clean` is run.
- The class `desktop only` can be applied to controls and other elements that are helpful but not needed for mobile.
- Links, ie. theme and fork, are automatically generated but do not work in development as they link to the repo's master branch.
