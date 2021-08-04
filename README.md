# Sass Basic

## Hamburger menu:
### [Github Page](https://neczpal.github.io/scss-hamburger-menu/)

### How to Build
 * `npm run build` - Builds plain nesting variant [`style.scss`](https://github.com/neczpal/scss-hamburger-menu/blob/master/src/scss/style.scss)
 * `npm run build-bem` - Builds BEM variant [`style-bem.scss`](https://github.com/neczpal/scss-hamburger-menu/blob/master/src/scss/style-bem.scss)

### How to Run

* Open the index.html in `dist/index.html`

## Operations:

#### EQUALITY

* ###### Numbers
  * `1px == 1` => `false`
  * `1px == 1px` => `true`
  * `10px == 1cm` => `false`
  * `48px == 0.5in` => `true`
  * `0.9999999999999999 == 1` => `true`
* ###### Strings
  * `Arial == 'Arial'` => `true`
  * `Arial == "Arial"` => `true`
  * `'Arial' == "Arial"` => `true`
* ###### Booleans
  * `true == true` => `true`
  * `false != true` => `true`
#### RELATIONS
* `100 > 50` => `true`
* `10px < 17px` => `true`
* `97px >= 1in` => `true`
* `1000ms <= 1s` => `true`
#### MATH
* `10s + 5s` => `15s`
* `10s - 50ms` => `9.95s`
* `10px * 2` => `20px`
* `10px * 2px` => `20px*px` - **DON'T MULTIPLY UNITS WITH UNITS**
* `10px / 2px` => `10px/2px` - **DON'T USE `/` WITH NUMBERS**
* `math.div(10px / 2)` => `5px`
* `11px % 2` => `1px`
#### BOOLEAN
* `not false` => `true`
* `true or false` => `true`
* `true and true` => `true`

#### STRING
```
$postfix: "--10";
.container#{$postfix}::before {
    font: 16px/16px "Times " + "New Roman", Times, serif;
    content: track - list;

    .interpolation {
        content: #{"track" + "list"};
    }
}
```
=>
```
.container--10::before {
  font: 16px/16px "Times New Roman", Times, serif;
  content: track-list;
}
.container--10::before .interpolation {
  content: tracklist;
}
```

### Further resources

* #### [Sass playground](https://www.sassmeister.com/)
* #### [Sass documentation](https://sass-lang.com/documentation)