# Ridiculously Responsive Social Sharing Buttons Plus
Social sharing buttons that you can drop into any website with attractive SVG-based icons, small download, and browser compatibility.
RRSSB+ automatically adjusts to different screen sizes by tweaking sizes, splitting buttons evenly onto multiple rows and hiding the labels.

The library offers consistently styled buttons for all sites.  No 3rd-party scripts (such as from Facebook), with the inherent overheads and different button designs.

![Two rows of buttons with prefix and label](https://www.drupal.org/files/rrssb_2x3.png) &nbsp; ![Small buttons](https://www.drupal.org/files/rrssb_small_0.PNG) &nbsp; ![Vertical align](https://www.drupal.org/files/rrssb_vertical.PNG)

Developed by [**AlbanyWeb**](http://www.albanyweb.co.uk/).
Based on [**RRSSB**](https://github.com/kni-labs/rrssb) "Ridiculously Responsive Social Sharing Buttons" by [**KNI**](http://www.kurtnoble.com).

## Installation instructions
If you use the Drupal CMS then you can automatically install this library with a [module](https://www.drupal.org/project/rrssb) — see [demo](https://www.albanyweb.co.uk/rrssb-plus). If you use Backdrop CMS you can install a [module which bundles this library](https://github.com/backdrop-contrib/rrssb) through the Project Installer interface.

Otherwise, you can examine the source of the demo page to see how to do it.  Search for `<div class="rrssb">` to find the HTML for the buttons.  You need to load `rrssb.min.js` and `rrssb.css`.  To configure this library, make a call to `rrssbConfigAll`.

## Main changes from RRSSB
- Allow buttons to split onto multiple rows, ensuring the rows stay even.
- Buttons size automatically stays usable and clear.  As a rule we don't want huge buttons on a huge screen or tiny ones on a tiny screen, which you can get with RRSSB.
RRSSB+ offers a configurable default size, and a configurable percentage allowable shrink.
- Whitespace around icons and text is consistent at all sizes.  With RRSSB, the spacing varies with button size.  At "normal width" there is lots of space, hence smaller fonts and icons that are harder to read.
Grow the screen, and you see the "large format", and it's different — and we think a better balance.
By default, RRSSB is similar to the large format, but with slightly larger icons.
- Uniform responsiveness applied simultaneously to all buttons.  In contrast RRSSB hides the labels one-by-one.
That's not an approach we are familiar with on mainstream websites, and we feel it looks odd, as if there is a bug.
- Support button prefix text such as "Share this page".  The RRSSB demo page has text like that although not responsive,
and hard-coded into the page rather than being part of the library.
- Configurable settings to control appearance.

## Performance changes
- Use background image instead of inline SVG.  Gives smaller page sizes, reduced server load and smaller caches.
- Smaller JS and CSS files for faster download.
- Simpler script executes a lot less lines of code for smoother resizing.
- Reduced DOM size: store working data as data() not attr().

## Compatibility changes
- Compatible with older releases of jQuery - remove specific requirement for jQuery 1.10
- Designed for integration into a CMS such as [Drupal](https://www.drupal.org/project/rrssb) and [Backdrop](https://backdropcms.org/project/rrssb).
