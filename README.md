# sass-svg-uri

A Sass module with [Jakob Eriksen's](http://codepen.io/jakob-e/pen/doMoML) function to encode SVG markup into optimized `data:` URIs. Uses [Hugo Giraudel's str-replace function](http://sassmeister.com/gist/1b4f2da5527830088e4d) to percent-encode characters that aren’t URL-safe.

As of version 2.0 this only supports Dart Sass `1.33.0` and above.

## Usage

Import the module and use the `encode` function.

```scss
@use "sass-svg-uri";

.icon {
    background-image: sass-svg-uri.encode('<svg xmlns="http://www.w3.org/2000/svg"> ... </svg>');
}
```

This would output:

```css
.icon {
    background-image: url("data:image/svg+xml,%3Csvg xmlns='http://www.w3.org/2000/svg'%3E% ... %3C/svg%3E");
}
```

To learn more:

* [CSS-Tricks: Probably Don’t Base64 SVG](https://css-tricks.com/probably-dont-base64-svg/)
* [Codepen: Optimizing SVGs in data URIs](http://codepen.io/Tigt/post/optimizing-svgs-in-data-uris)
* [Introducing CSS Modules](https://css-tricks.com/introducing-sass-modules/)