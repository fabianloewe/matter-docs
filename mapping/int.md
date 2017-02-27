# Integer

The integer type \(defined as `Int`\) represents a **non-floating point** number. At the moment it can only be created as a decimal number.

 It can also be auto-converted like [`String`](/mapping/available-types.md)with the exception that each string in the syntax rule must only consist of digits.

#### Examples

**Definition in **[**`Mapping`**](/mapping.md)**:**

```ruby
example = 42
```

`example` represents the number `42`.

**Auto-conversion:**

```ruby
ExampleType < Matter:
  Syntax:
    valid   = "0123" ("4567" | "3210")
    invalid = "0123" "bla"
  Mapping:
    valid -> Int        # Valid
    invalid -> Int      # Invalid
    #invalid -> String  # Valid
```



