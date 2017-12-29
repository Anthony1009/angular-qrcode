Angular QR Code
===============

````html
<qrcode></qrcode>
````

An AngularJS directive to create QR Codes using Kazuhiko Arase’s [qrcode-generator](https://github.com/kazuhikoarase/qrcode-generator) library.

[See it in action](http://monospaced.github.io/angular-qrcode).
Forked from Monospaced's repository.


Usage
-----

as element

````html
<qrcode data="string"></qrcode>
````

with QR options

````html
<qrcode data="string" version="2" error-correction-level="Q" size="200" color="#fff" ba kground="#000"></qrcode>
````

as a downloadable image

````html
<qrcode data="string" download></qrcode>
````

as a link to URL

````html
<qrcode data="http://example.com" href="http://example.com"></qrcode>
````

`download` and `href` can’t be used on the same element (if `download` is present, `href` will be ignored)

with expressions, observe changes

````html
<qrcode version="{{version}}" error-correction-level="{{level}}" size="{{size}}" data="{{var}}" href="{{var}}" color="{{color}}" background="{{background}}" padding="{{padding}}" name="{{name}}" download></qrcode>
````

Options
-------

Permitted values

* `version`: `1–40`  (default: `5`) _- if required, will be auto-incremented to contain data given_

* `error-correction-level`: `L`, `M`, `Q`, `H` (default: `M`)

* `size`: `integer` (default: `size` is calculated automatically)

* `download`: `boolean` (default: `false`)

* `href`: `url` as `string`

* `color`: `hex` as `string` (default: `#000`)

* `background`: `hex` as `string` (default: `#fff`)

* `padding`: `integer` (default: `0`)

* `name`: `string` (default: `qrcode`) _- name of image that might be downloaded in png format._

The amount of data (measured in bits) must be within capacity according to the `version` and `error correction level`, see http://www.qrcode.com/en/about/version.html.

Demo
----------------

[monospaced.github.io/angular-qrcode](http://monospaced.github.io/angular-qrcode)

Reference
----------------

[QR Code versions](http://www.qrcode.com/en/about/version.html)

[QR Code error correction](http://www.qrcode.com/en/about/error_correction.html)
