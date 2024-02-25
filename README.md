<!--

@license Apache-2.0

Copyright (c) 2021 The Stdlib Authors.

Licensed under the Apache License, Version 2.0 (the "License");
you may not use this file except in compliance with the License.
You may obtain a copy of the License at

   http://www.apache.org/licenses/LICENSE-2.0

Unless required by applicable law or agreed to in writing, software
distributed under the License is distributed on an "AS IS" BASIS,
WITHOUT WARRANTIES OR CONDITIONS OF ANY KIND, either express or implied.
See the License for the specific language governing permissions and
limitations under the License.

-->


<details>
  <summary>
    About stdlib...
  </summary>
  <p>We believe in a future in which the web is a preferred environment for numerical computation. To help realize this future, we've built stdlib. stdlib is a standard library, with an emphasis on numerical and scientific computation, written in JavaScript (and C) for execution in browsers and in Node.js.</p>
  <p>The library is fully decomposable, being architected in such a way that you can swap out and mix and match APIs and functionality to cater to your exact preferences and use cases.</p>
  <p>When you use stdlib, you can be absolutely certain that you are using the most thorough, rigorous, well-written, studied, documented, tested, measured, and high-quality code out there.</p>
  <p>To join us in bringing numerical computing to the web, get started by checking us out on <a href="https://github.com/stdlib-js/stdlib">GitHub</a>, and please consider <a href="https://opencollective.com/stdlib">financially supporting stdlib</a>. We greatly appreciate your continued support!</p>
</details>

# linspace

[![NPM version][npm-image]][npm-url] [![Build Status][test-image]][test-url] [![Coverage Status][coverage-image]][coverage-url] <!-- [![dependencies][dependencies-image]][dependencies-url] -->

> Generate a linearly spaced numeric array.



<section class="usage">

## Usage

```javascript
import linspace from 'https://cdn.jsdelivr.net/gh/stdlib-js/array-base-linspace@v0.2.1-esm/index.mjs';
```

#### linspace( start, stop, length )

Generates a linearly spaced numeric `array`.

```javascript
var arr = linspace( 0, 100, 6 );
// returns [ 0, 20, 40, 60, 80, 100 ]
```

</section>

<!-- /.usage -->

<section class="notes">

## Notes

-   The function assumes that `length` is greater than or equal to `2`.

-   The output `array` is guaranteed to include the `start` and `stop` values. Beware, however, that values between `start` and `stop` are subject to floating-point rounding errors. Hence,

    ```javascript
    var arr = linspace( 0, 1, 3 );
    // returns [ 0, ~0.5, 1 ]
    ```

    where `arr[1]` is only guaranteed to be approximately equal to `0.5`. If you desire more control over element precision, consider using [`roundn`][@stdlib/math/base/special/roundn]:

    ```javascript
    import roundn from 'https://cdn.jsdelivr.net/gh/stdlib-js/math-base-special-roundn@esm/index.mjs';

    // Create an array subject to floating-point rounding errors:
    var arr = linspace( 0, 1, 21 );

    // Round each value to the nearest hundredth:
    var i;
    for ( i = 0; i < arr.length; i++ ) {
        arr[ i ] = roundn( arr[ i ], -2 );
    }
    console.log( arr.join( '\n' ) );
    ```

</section>

<!-- /.notes -->

<section class="examples">

## Examples

<!-- eslint no-undef: "error" -->

```html
<!DOCTYPE html>
<html lang="en">
<body>
<script type="module">

import linspace from 'https://cdn.jsdelivr.net/gh/stdlib-js/array-base-linspace@v0.2.1-esm/index.mjs';

// Create arrays of varying lengths:
var out = linspace( 0, 10, 10 );
console.log( out );

out = linspace( 0, 10, 11 );
console.log( out );

out = linspace( 0, 10, 21 );
console.log( out );

// Create an array with decremented values:
out = linspace( 10, 0, 11 );
console.log( out );

</script>
</body>
</html>
```

</section>

<!-- /.examples -->

<!-- Section for related `stdlib` packages. Do not manually edit this section, as it is automatically populated. -->

<section class="related">

</section>

<!-- /.related -->

<!-- Section for all links. Make sure to keep an empty line after the `section` element and another before the `/section` close. -->


<section class="main-repo" >

* * *

## Notice

This package is part of [stdlib][stdlib], a standard library with an emphasis on numerical and scientific computing. The library provides a collection of robust, high performance libraries for mathematics, statistics, streams, utilities, and more.

For more information on the project, filing bug reports and feature requests, and guidance on how to develop [stdlib][stdlib], see the main project [repository][stdlib].

#### Community

[![Chat][chat-image]][chat-url]

---

## License

See [LICENSE][stdlib-license].


## Copyright

Copyright &copy; 2016-2024. The Stdlib [Authors][stdlib-authors].

</section>

<!-- /.stdlib -->

<!-- Section for all links. Make sure to keep an empty line after the `section` element and another before the `/section` close. -->

<section class="links">

[npm-image]: http://img.shields.io/npm/v/@stdlib/array-base-linspace.svg
[npm-url]: https://npmjs.org/package/@stdlib/array-base-linspace

[test-image]: https://github.com/stdlib-js/array-base-linspace/actions/workflows/test.yml/badge.svg?branch=v0.2.1
[test-url]: https://github.com/stdlib-js/array-base-linspace/actions/workflows/test.yml?query=branch:v0.2.1

[coverage-image]: https://img.shields.io/codecov/c/github/stdlib-js/array-base-linspace/main.svg
[coverage-url]: https://codecov.io/github/stdlib-js/array-base-linspace?branch=main

<!--

[dependencies-image]: https://img.shields.io/david/stdlib-js/array-base-linspace.svg
[dependencies-url]: https://david-dm.org/stdlib-js/array-base-linspace/main

-->

[chat-image]: https://img.shields.io/gitter/room/stdlib-js/stdlib.svg
[chat-url]: https://app.gitter.im/#/room/#stdlib-js_stdlib:gitter.im

[stdlib]: https://github.com/stdlib-js/stdlib

[stdlib-authors]: https://github.com/stdlib-js/stdlib/graphs/contributors

[umd]: https://github.com/umdjs/umd
[es-module]: https://developer.mozilla.org/en-US/docs/Web/JavaScript/Guide/Modules

[deno-url]: https://github.com/stdlib-js/array-base-linspace/tree/deno
[deno-readme]: https://github.com/stdlib-js/array-base-linspace/blob/deno/README.md
[umd-url]: https://github.com/stdlib-js/array-base-linspace/tree/umd
[umd-readme]: https://github.com/stdlib-js/array-base-linspace/blob/umd/README.md
[esm-url]: https://github.com/stdlib-js/array-base-linspace/tree/esm
[esm-readme]: https://github.com/stdlib-js/array-base-linspace/blob/esm/README.md
[branches-url]: https://github.com/stdlib-js/array-base-linspace/blob/main/branches.md

[stdlib-license]: https://raw.githubusercontent.com/stdlib-js/array-base-linspace/main/LICENSE

[@stdlib/math/base/special/roundn]: https://github.com/stdlib-js/math-base-special-roundn/tree/esm

</section>

<!-- /.links -->
