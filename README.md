# [Google Material Design Analysis](http://edwardzhu.me/google-material-design)

My Design Analysis of Material Design by Google for WTRG 3035. I give an introduction to the design guidelines,  and incorporated material design within the site as well.

Check out [the review here](http://zhued.github.io/google-material-design/).



#What I used

## Material.js

`Material.js` is a jQuery plugin that adds some magic to your markup and allows Material Design for Bootstrap to style some elements like inputs, checkboxes, radios etc.

### Functions

* `$.material.init()` - shortcut to run all the following commands:
* `$.material.ripples()` will apply ripples.js to the default elements.
* `$.material.input()` will enable the MD style to the text inputs, and other kind of inputs (number, email, file etc).
* `$.material.checkbox():` will enable the MD style to the checkboxes (remember to follow the markup guidelines explained in the [Inputs section](#inputs).
* `$.material.radio():` will enable the MD style to the checkboxes (remember to follow the markup guidelines explained in the Inputs section.

### Apply Material.js only to specific elements

Every function expects an optional value that will be used as a selector for the function; for example,
`$.material.ripples("#selector, #foobar")` will apply Ripples.js only to `#selector` and `#foobar`.
The functions that allows an optional selector are `$.material.ripples`, `$.material.input`, `$.material.checkbox` and `$.material.radio`.

You can even override the default values using the `$.material.options` function. The default values are:

    $.material.options = {
        "withRipples": ".btn:not(.btn-link), .card-image, .navbar a:not(.withoutripple), .nav-tabs a:not(.withoutripple), .withripple",
        "inputElements": "input.form-control, textarea.form-control, select.form-control",
        "checkboxElements": ".checkbox > label > input[type=checkbox]",
        "radioElements": ".radio > label > input[type=radio]"
    }

### Arrive.js support

If you need to dynamically add elements to your DOM then you may need to include `Arrive.js` before `Material.js`. This will automatically apply `Material.js` to every new element added via JavaScript.

## Plugins

Material Design for Bootstrap comes with styling support for various external scripts:

### SnackbarJS

Create snackbars and toasts with the [SnackbarJS plugin](https://github.com/FezVrasta/snackbarjs). The default toast style is the squared one (snackbar style). If you like to use the rounded style (toast style), please add the `toast` class to the `style` option of SnackbarJS.

### RipplesJS

This is part of the Material Design for Bootstrap project and is a plain JavaScript script which creates the ripple effect when clicking on the specified elements.
At the moment RipplesJS does not have its own repository but it will probably have one in the future.

You may want to set a custom color to the ripples of a specific element, to do so write:

    <button class="btn btn-default" data-ripple-color="#F0F0F0">Custom ripple</button>

### noUiSlider

Make cross-browser sliders and get them styled with Material Design thanks to the support provided by this theme.
Read more about [noUiSlider here](http://refreshless.com/nouislider/).

### Dropdown.js

Finally a dropdown plugin that transforms select inputs in nice dropdowns and does not drive you crazy.
Read more about [Dropdown.js here](https://github.com/FezVrasta/dropdown.js).

### Selectize.js

Transform select and multi-select inputs into advanced text inputs. Material Design for BS provides a full replacement of the plugin's CSS, so don't include it.
Read more about [selectize.js](http://brianreavis.github.io/selectize.js/).

## Compatibility

Currently, Material Design for Bootstrap supports Google Chrome (tested v37+), Mozilla Firefox (tested 30+), and Internet Explorer (tested 11+). Mobile browsers are not currently tested but they may work.
