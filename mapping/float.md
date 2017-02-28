# Floating pointer number

The `Float` type represents a floating point number. At the moment it can only be created as a decimal number.

It can also be auto-converted like [`String`](/mapping/available-types.md)with the exception that each string in the syntax rule must only consist of digits **and one dot between them**.

### Examples

##### **Definition in **[`Mapping`](/mapping.md)**:**

```ruby
example = 3.142
```

`example` represents the number `42`.

##### **Auto-conversion:**

```ruby
ExampleType < Matter:
  Syntax:
    valid    = "0123." ("4567" | "3210")
    invalid1 = "0123" "9876"
    invalid2 = "0123." "bla"
  Mapping:
    valid -> Float       # Valid
    #valid -> Int        # Invalid
    invalid1 -> Float    # Invalid
    #invalid1 -> Int     # Valid
    invalid2 -> Float    # Invalid
    #invalid2 -> String  # Valid
```

Only `valid` can be converted to `Float` because its rule is made of strings containing just digits and exactly one dot.

`invalid1` could be legally converted to [`Int`](//mapping/int.md) while `invalid2` just is a valid [`String`](/mapping/available-types.md).

