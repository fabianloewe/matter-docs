## Concatenation

A _concatenation_ appends one rule to another. This means that to be valid, the first rule must be parsed followed by the second one immediately.

**Symbol: **Whitespace



#### Example

```ruby
example = "Hello world" "!"
```

In the example above the string `Hello world` is expected first then `!` must immediately follow.

**Valid string: **`Hello world!`

**Invalid strings: **`Hello world !` , `Hello world`

