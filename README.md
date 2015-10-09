# SASS SVG URI

This is just a simple module with [Jakob Eriksen's function](http://codepen.io/jakob-e/pen/doMoML) for easy use in projects. Uses [Hugo Giraudel's str-replace function](http://sassmeister.com/gist/1b4f2da5527830088e4d) to replace invalid characters in the SVG as a data uri.

## Usage

Just import the file and use the function, no dependencies.

```scss
@import "sass-svg-uri/svg-uri";

.icon {
    background-image: svg-uri('<svg xmlns="http://www.w3.org/2000/svg"> ... </svg>');
}
```

Would output:

```css
.icon {
    background-image: url("data:image/svg+xml;charset=utf8,%3Csvg xmlns='http://www.w3.org/2000/svg'%3E% ... %3C/svg%3E");
}
```

To know more:

* [CSS-Tricks: Probably Don’t Base64 SVG](https://css-tricks.com/probably-dont-base64-svg/)
* [Codepen: Optimizing SVGs in data URIs](http://codepen.io/Tigt/post/optimizing-svgs-in-data-uris)

