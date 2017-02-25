### Alternation

```ruby
example = "Hello world" "!" | "."
```

**Symbol:** TODO: add name \(`|`\)

**Operation: **The first part or the second is expected. In the example above this means the string `Hello world` is expected first then `!` or `.` can follow. So both `Hello world!` and `Hello world.`would be accept while for example `Hello world?` would **not**. To make an alternation better visible consider using grouping.

