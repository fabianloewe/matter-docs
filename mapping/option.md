# Optional

An `Optional` represents a mutable set of one or no value. It is returned by an [_option_](//syntax/option.md) in [`Syntax`](//syntax/README.md) and **cannot** be created manually. The only valid member is at index zero \(`0`\) and no other indexes can be accessed.

### Examples

##### **Access the element:**

```ruby
ExampleType < Matter:
  Syntax:
    example = [ "Bla" ]
  Mapping:
    example -> String:
      example.0
```

The mapping of `example` either returns `Bla` or throws an error and stops parsing immediately.

