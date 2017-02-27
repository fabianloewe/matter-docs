## Alternation

An \_alternation \_makes it possible to define one or more alternatives which are tried from left to right. Once one rule was correctly evaluated no other possibilites are checked and the parser moves on to the next rule.

**Symbol:** TODO: add name \(`|`\)

#### Example

```ruby
example = "Hello world" "!" | "."
```

This example expectes `Hello world` first then either `!` or `.` can follow.

**Valid strings: **`Hello world!` , `Hello world.`

**Invalid strings:** `Hello world !` , `Hello world!.`

