Deprecated
==========

Is npm bugging you about this module being deprecated? You are probably depending on this module via the [source-map-resolve](https://github.com/lydell/source-map-resolve) package, which is [deprecated too](https://github.com/lydell/source-map-resolve#deprecated).

If you are looking for a way to normalize between Windows and Unix paths, just do it in whatever way makes sense for your project. This module is just weird.

Overview [![Build Status](https://travis-ci.org/lydell/urix.png?branch=master)](https://travis-ci.org/lydell/urix)
========

Makes Windows-style paths more unix and URI friendly. Useful if you work with
paths that eventually will be used in URLs.

```js
var urix = require("urix")

// On Windows:
urix("c:\\users\\you\\foo")
// /users/you/foo

// On unix-like systems:
urix("c:\\users\\you\\foo")
// c:\users\you\foo
```


Installation
============

`npm install urix`

```js
var urix = require("urix")
```


Usage
=====

### `urix(path)` ###

On Windows, replaces all backslashes with slashes and uses a slash instead of a
drive letter and a colon for absolute paths.

On unix-like systems it is a no-op.


License
=======

[The X11 (“MIT”) License](LICENSE).
