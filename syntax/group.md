# Group

A _group_ creates a sub-rule by containing one or more other rules. It can \(and should\) also be used to make larger rules like an huge [alternation](//syntax/alternation.md) more outstanding.

**Symbol:** Square brackets \(`[` and `]` \)

### Example

```ruby
example = "Hello world" [ "!" ]
```

`Hello world` is expected first then `!` can immediately follow.

**Valid strings:** `Hello world` , `Hello world!`

**Invalid strings: **`Hello world.` , `Hello world !`

