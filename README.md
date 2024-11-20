# Yielder

Unfold values on-demand from a function.

[![Package Version](https://img.shields.io/hexpm/v/gleam_yielder)](https://hex.pm/packages/gleam_yielder)
[![Hex Docs](https://img.shields.io/badge/hex-docs-ffaff3)](https://hexdocs.pm/gleam_yielder/)

```sh
gleam add gleam_yielder@1
```
```gleam
import gleam/yielder

pub fn main() {
  yielder.unfold(2, fn(acc) { yielder.Next(acc, acc * 2) })
  |> yielder.take(5)
  |> yielder.to_list
  // -> [2, 4, 8, 16, 32]
}
```

Further documentation can be found at <https://hexdocs.pm/gleam_yielder>.
