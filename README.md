<!--

@license Apache-2.0

Copyright (c) 2018 The Stdlib Authors.

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

# Raised Cosine Random Numbers

[![NPM version][npm-image]][npm-url] [![Build Status][test-image]][test-url] [![Coverage Status][coverage-image]][coverage-url] <!-- [![dependencies][dependencies-image]][dependencies-url] -->

> Create a [readable stream][readable-stream] for generating pseudorandom numbers drawn from a [raised cosine][cosine] distribution.









<!-- Section for describing a command-line interface. -->



<section class="cli">



<section class="installation">

## Installation

To use as a general utility, install the CLI package globally

```bash
npm install -g @stdlib/random-streams-cosine-cli
```

</section>
<!-- CLI usage documentation. -->


<section class="usage">

## Usage

```text
Usage: random-cosine [options] <mu> <s>

Options:

  -h,  --help               Print this message.
  -V,  --version            Print the package version.
       --sep sep            Separator used to join streamed data. Default: '\n'.
  -n,  --iter iterations    Number of pseudorandom numbers.
       --seed seed          Pseudorandom number generator seed.
       --state filepath     Path to a file containing the pseudorandom number
                            generator state.
       --snapshot filepath  Output file path for saving the pseudorandom number
                            generator state upon exit.
```

</section>

<!-- /.usage -->

<!-- CLI usage notes. Make sure to keep an empty line after the `section` element and another before the `/section` close. -->

<section class="notes">

## Notes

-   In accordance with POSIX convention, a trailing newline is **always** appended to generated output prior to exit.
-   Specifying a "snapshot" file path is useful when wanting to resume pseudorandom number generation due to, e.g., a downstream failure in an analysis pipeline. Before exiting, the process will store the pseudorandom number generator state in a file specified according to a provided file path. Upon loading a snapshot (state), the process will generate pseudorandom numbers starting from the loaded state, thus avoiding having to seed and replay an entire analysis.

</section>

<!-- /.notes -->

<!-- CLI usage examples. -->

<section class="examples">

## Examples

```bash
$ random-cosine 0.0 1.0 -n 10 --seed 1234
```

</section>

<!-- /.examples -->

</section>

<!-- /.cli -->

<!-- Section for related `stdlib` packages. Do not manually edit this section, as it is automatically populated. -->

<section class="related">

## See Also

-   <span class="package-name">[`@stdlib/random-streams-cosine`][@stdlib/random-streams-cosine]</span><span class="delimiter">: </span><span class="description">create a readable stream for generating pseudorandom numbers drawn from a raised cosine distribution.</span>
-   <span class="package-name">[`@stdlib/random-base/cosine`][@stdlib/random/base/cosine]</span><span class="delimiter">: </span><span class="description">raised cosine distributed pseudorandom numbers.</span>
-   <span class="package-name">[`@stdlib/random-iter/cosine`][@stdlib/random/iter/cosine]</span><span class="delimiter">: </span><span class="description">create an iterator for generating pseudorandom numbers drawn from a raised cosine distribution.</span>

</section>

<!-- /.related -->

<!-- Section for all links. Make sure to keep an empty line after the `section` element and another before the `/section` close. -->


<section class="main-repo" >

* * *

## Notice

This package is part of [stdlib][stdlib], a standard library for JavaScript and Node.js, with an emphasis on numerical and scientific computing. The library provides a collection of robust, high performance libraries for mathematics, statistics, streams, utilities, and more.

For more information on the project, filing bug reports and feature requests, and guidance on how to develop [stdlib][stdlib], see the main project [repository][stdlib].

### Community

[![Chat][chat-image]][chat-url]

---

## License

See [LICENSE][stdlib-license].


## Copyright

Copyright &copy; 2016-2025. The Stdlib [Authors][stdlib-authors].

</section>

<!-- /.stdlib -->

<!-- Section for all links. Make sure to keep an empty line after the `section` element and another before the `/section` close. -->

<section class="links">

[npm-image]: http://img.shields.io/npm/v/@stdlib/random-streams-cosine-cli.svg
[npm-url]: https://npmjs.org/package/@stdlib/random-streams-cosine-cli

[test-image]: https://github.com/stdlib-js/random-streams-cosine/actions/workflows/test.yml/badge.svg?branch=main
[test-url]: https://github.com/stdlib-js/random-streams-cosine/actions/workflows/test.yml?query=branch:main

[coverage-image]: https://img.shields.io/codecov/c/github/stdlib-js/random-streams-cosine/main.svg
[coverage-url]: https://codecov.io/github/stdlib-js/random-streams-cosine?branch=main

<!--

[dependencies-image]: https://img.shields.io/david/stdlib-js/random-streams-cosine.svg
[dependencies-url]: https://david-dm.org/stdlib-js/random-streams-cosine/main

-->

[chat-image]: https://img.shields.io/gitter/room/stdlib-js/stdlib.svg
[chat-url]: https://app.gitter.im/#/room/#stdlib-js_stdlib:gitter.im

[stdlib]: https://github.com/stdlib-js/stdlib

[stdlib-authors]: https://github.com/stdlib-js/stdlib/graphs/contributors

[cli-section]: https://github.com/stdlib-js/random-streams-cosine#cli
[cli-url]: https://github.com/stdlib-js/random-streams-cosine/tree/cli
[@stdlib/random-streams-cosine]: https://github.com/stdlib-js/random-streams-cosine/tree/main

[umd]: https://github.com/umdjs/umd
[es-module]: https://developer.mozilla.org/en-US/docs/Web/JavaScript/Guide/Modules

[deno-url]: https://github.com/stdlib-js/random-streams-cosine/tree/deno
[deno-readme]: https://github.com/stdlib-js/random-streams-cosine/blob/deno/README.md
[umd-url]: https://github.com/stdlib-js/random-streams-cosine/tree/umd
[umd-readme]: https://github.com/stdlib-js/random-streams-cosine/blob/umd/README.md
[esm-url]: https://github.com/stdlib-js/random-streams-cosine/tree/esm
[esm-readme]: https://github.com/stdlib-js/random-streams-cosine/blob/esm/README.md
[branches-url]: https://github.com/stdlib-js/random-streams-cosine/blob/main/branches.md

[stdlib-license]: https://raw.githubusercontent.com/stdlib-js/random-streams-cosine/main/LICENSE

[stream]: https://nodejs.org/api/stream.html

[object-mode]: https://nodejs.org/api/stream.html#stream_object_mode

[readable-stream]: https://nodejs.org/api/stream.html

[cosine]: https://en.wikipedia.org/wiki/Raised_cosine_distribution

[@stdlib/array/uint32]: https://github.com/stdlib-js/array-uint32

<!-- <related-links> -->

[@stdlib/random/base/cosine]: https://github.com/stdlib-js/random-base-cosine

[@stdlib/random/iter/cosine]: https://github.com/stdlib-js/random-iter-cosine

<!-- </related-links> -->

</section>

<!-- /.links -->
