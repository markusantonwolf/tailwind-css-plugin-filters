# Tailwind CSS Plugin Filter utilities

This plugins adds some filter utilities to your configuration. Based on the default colors this plugin renders the following utilities for you:

- drop-shadow
    - drop-shadow-{SIZE}
        - sizex: sm, md, lg, xl and 2xl
    - drop-shadow-{COLOR}-{INDEX}
        - Tailwind CSS default colors
- backdrop-blur
    - Sizes from 1 - 5
- bg-blur
    - Sizes from 1 - 5
- blur
    - Sizes from 1 - 5

The drop shadow utility uses CSS custom properties to make it easier to define your favorite style. **You can find a list of all generated utilities in the [list of all utilities](https://github.com/markusantonwolf/tailwindcss-filters/blob/master/public/utilities.css).**

## Install

1. Install the plugin:

  ```bash
  # Using npm
  npm install @markusantonwolf/tailwindcss-filters --save-dev

  # Using Yarn
  yarn add @markusantonwolf/tailwindcss-filters -D
  ```

2. Add it to your `tailwind.config.js` file:

  ```js
  // tailwind.config.js
  module.exports = {
    // ...
    plugins: [
      require('@markusantonwolf/tailwindcss-filters')
    ]
  }
  ```

## Usage

```html
<div class="drop-shadow drop-shadow-xl drop-shadow-gray-100"></div>
<div class="backdrop-blur-5"></div>
<div class="blur-5"></div>
```

## Features

-   CSS filters:
    - backdrop-filter: blur
    - filter: drop-shadow
    - filter: blur
-   Options:
     - variants: defines the variants to be created | default: ["responsive"]
     - utilities: defines the utilities to be created | default: ["drop-shadow","blur","backdrop-blur"]
     - debug: shows the new utilities | default: false

## Options example

```js
// tailwind.config.js
module.exports = {
// ...
    plugins: [
        require("@markusantonwolf/tailwindcss-filters")({
            variants: ["responsive"],
            utilities: ["drop-shadow", "blur", "backdrop-blur"],
            debug: false,
        }),
    ]
}
```

## Licence

Tailwind CSS Plugin Filter utilities is released under the [MIT license](https://github.com/markusantonwolf/tailwindcss-filters/blob/master/licence.md) & supports modern environments.

## Copyright

© 2020 Markus A. Wolf
<https://www.markusantonwolf.com>
