# Device Media Query

A Sass mixin library that allows for defining media queries for various devices with logical operators.

## How It Works

The library provides a mixin called device that takes in logical operators and values corresponding to screen widths. You can create complex media queries using operators like >, >=, <, and <= combined with predefined device variables or custom values.

## Variables Definition and How to Override Them

The library includes predefined variables for common device sizes:

```scss
$phone: 480px;
$phone-landscape: 812px;
$tablet: 1024px;
$tablet-landscape: 1366px;
$desktop: 1920px;
$laptop: 1920px;
$screen-4k: 3840px;
```
You can override these variables by defining them in your Sass file before importing the library:

```scss
$phone: 500px; // Your custom value

@import 'device_media_query/src/index';
```

## Logic Operators

You can use the following logical operators with the device mixin:

- > : greater than
- >= : greater than or equal to
- < : less than
- <= : less than or equal to

## How to Install from Git

1) Clone the repository:

```bash
git clone https://github.com/yourusername/device_media_query.git
```

2) Import the library in your Sass file:

```scss
@import 'path/to/device_media_query/src/index';
```

## How to Install with npm

2) Install the package:

```bash
npm install device-media-query
```

3) Import the library in your Sass file using either @import:

```scss
@import 'device-media-query/src/index';
```

## Example Usage

Here's an example of how you can use the device mixin:

```scss
@include device('>', $tablet, '<=', $desktop) {
  .my-class {
    font-size: 18px;
  }
}
```
This will generate a media query that applies the specified styles to screens greater than $phone and less than or equal to $tablet.
The rendered CSS will look like:

```css
@media (min-width: 1025px) and (max-width: 1920px) {
  .my-class {
    font-size: 18px;
  }
}
```

## License

This project is licensed under the GNU General Public License v3.0. See the [LICENSE](LICENSE) file for details.
