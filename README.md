# Underscore: `@_` macro

[![Build Status](https://travis-ci.org/kleinschmidt/Underscore.jl.svg?branch=master)](https://travis-ci.org/kleinschmidt/Underscore.jl)

[![Coverage Status](https://coveralls.io/repos/kleinschmidt/Underscore.jl/badge.svg?branch=master&service=github)](https://coveralls.io/github/kleinschmidt/Underscore.jl?branch=master)

[![codecov.io](http://codecov.io/github/kleinschmidt/Underscore.jl/coverage.svg?branch=master)](http://codecov.io/github/kleinschmidt/Underscore.jl?branch=master)

Provides a "threading" `@_` macro, shamelessly lifted from
[SplitApplyCombine.jl](https://github.com/JuliaData/SplitApplyCombine.jl)

This adds the ability for piping to use the `_` to create anonymous functions quickly and
easily.

## Example:

`@_ data |> reduce(+,_)` expands to `data |> x->reduce(+,x)`
