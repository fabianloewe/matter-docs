### Option

An _option_ is a rule which can be defined in the parsed string but doesn't have to. 

**Symbol: **



#### Example

```ruby
example = "Hello world" [ "!" ]
```

`Hello world` is expected first then `!` can immediately follow.

**Valid strings:** `Hello world` , `Hello world!` 

**Invalid strings: **`Hello world.` , `Hello world !`

