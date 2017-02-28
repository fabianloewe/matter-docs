# Repetition

A _repetition_ defines a rule which can occur multiple times.

## Zero or more times {#zero-or-more-rep}

This type of repetition can be parsed one or more times or not at all and still is valid. The star \(`*`\) behind the curly brackets \(`{` and `}`\) defines this rule.

### Example

```ruby
example = "Hello world" { "!" }*
```

`Hello world` is expected first then an exclamation mark \(`!`\) can immediately follow multiple times.

**Valid strings:** `Hello world` , `Hello world!!!`

**Invalid strings: **`Hello world.` , `Hello world !`

## One or more times

This type of repetition must be parsed at least one or more times to be valid. The plus sign \(`+`\) behind the curly brackets \(`{` and `}`\) defines this rule.

### Example

```ruby
example = "Hello world" { "!" }+
```

`Hello world` is expected first then at least one exclamation mark \(`!`\) must immediately follow.

**Valid strings:** `Hello world!` , `Hello world!!!`

**Invalid strings: **`Hello world` , `Hello world !!`

