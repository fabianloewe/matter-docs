## Bool

The `Bool` type represents either one of the two values `true` and `false`. Always use this type for boolean logic, never `0` and `1` like in e.g. the C language.

It can automatically be converted from `String` to one of its values and vice versa. Also it **can** be created in code like the example below shows.

### Examples

##### **Definition:**

```ruby
is-an-example = true
```

`is-an-example` is set to `true`. It is good practice to name your `Bool` variables like a question or something that can only be correct or not.

##### **Auto-conversion:**

```ruby
ExampleType < Matter:
  Syntax:
    example1 = "true"
    example2 = "correct"
  Mapping:
    example1 -> Bool # Valid
    example2 -> Bool # Invalid
```

The rule `example1` only contains one string which holds the string representation of `true`. 

Because "correct" is not a valid value for `Bool` `example2` cannot be converted.

