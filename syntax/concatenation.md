### Concatenation {#concatenation}

```ruby
example = "Hello world" "!"
```

**Symbol:** Whitespace

**Operation: **The part on which the whitespace follows must be successfully parsed first. Then the part behind the whitespace must be parsed correctly, too. In the example above this means the string `Hello world` is expected first then `!` must immediately follow. So `Hello world!` would be parsed successfully while for example `Hello world !` would **not**.
