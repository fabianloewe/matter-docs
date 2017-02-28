# Option

An _option_ is a rule which can be defined in the parsed string but doesn't have to.

**Symbol:** Square brackets \(`[` and `]` \)

### Example

```ruby
example = "Hello world" [ "!" ]
```

`Hello world` is expected first then an exclamation mark \(`!`\) can immediately follow.

**Valid strings:** `Hello world` , `Hello world!`

**Invalid strings: **`Hello world.` , `Hello world !`

#### 



