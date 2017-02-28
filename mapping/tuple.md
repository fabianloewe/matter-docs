# Tuple

A tuple represents a set of multiple values with optionally different types. It is returned by a [_concatenation_](//syntax/concatenation.md) in [`Syntax`](//syntax/README.md) and cannot be created manually at the moment nor get values appended. You can access each member of the `Tuple` by appending a dot followed by the index you are interested in. Counting starts at **zero **\(`0`\).

### Examples

##### **Access the second element:**

```ruby
ExampleType < Matter:
  Syntax:
    example = "This is " ("interesting" | "awesome")
  Mapping:
    example -> String:
      example.1
```

The mapping of `example` either returns `interesting` or `awesome`.

**Remainder:** If we leaved out the last line either `This is interesting` or `This is awesome` would be returned as the result of auto-conversion of [strings](/mapping/available-types.md).

##### **Tuple of tuples:**

```ruby
ExampleType < Matter:
  Syntax:
    example = "A " "tuple " (("of " "tuples") | ("can be " "nice"))
  Mapping:
    example -> String:
      example.2.1
```

We access the second element of third element \(the tuple inside\) of `example`. So either `tuples` or `nice` can be returned.

