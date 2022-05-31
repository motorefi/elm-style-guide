# Caribou's Elm style guide

This should generally copy https://github.com/motorefi/haskell-style-guide as much as possible.

## Module Organization

Modules should have this order so they can be read from top to bottom, minimizing jumping around

1. module name and export list
2. import block
3. exported functions
4. functions referenced in exported functions, in the order in which they are called in the exported functions
6. exported types
7. internal types

### Example

```elm
module Foo exposing (bar, foo, Foo)

import Stuff

foo : Foo
foo = fn1

bar : Bar
bar = fn2

fn1 = fn3

fn2 = Debug.todo ""

fn3 = Debug.todo""

type alias Foo = ...

type alias Bar = ...
```
