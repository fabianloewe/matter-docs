## String

The `String` is the type you might need most of the time. It simply contains a set of UTF-8 characters on which you can operate.

It is created by double quotes \(`"`\) and is the only type which is exactly the same in [_Syntax_](//syntax/README.md) and [_Mapping_](/mapping.md). It can be automatically converted from any syntax rules only consisting of other rules and strings \(no custom types\).

#### Examples

**Definition:**

```ruby
example = "Indeed this is a string"
```

`example` represents the character set `Indeed this is a string`.

**Auto-conversion:**

```ruby
ExampleType < Matter:
  Syntax:
    example = "This string can be auto-converted" (("." " Yeah!") | ("?" " Yes!"))
  Mapping:
    example -> String    # Valid
```

The rule `example` is only made of rules containing or working with strings. So no errors will occur.

