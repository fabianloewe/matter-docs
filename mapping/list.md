# List

A `List` represents a mutable set of multiple values of one type. It is returned by a [_repetition_](/syntax/repetition.md) in [`Syntax`](//syntax/README.md) and **can** be created manually. You can access each member of the `List` by appending a dot followed by the index you are interested in. Counting starts at **zero **\(`0`\).

#### Notes

* To use a variable as the index call the `at` method.
* If you get a `List` from a [_zero-or-more-times repetition_](/syntax/repetition.md#zero-or-more-times), check that the list is not empty by calling `not-empty`.

### Examples

##### **Access the first element:**

```ruby
ExampleType < Matter:
  Syntax:
    example = { "Bla" }+
  Mapping:
    example -> String:
      example.0
```

The mapping of `example` always returns `Bla`. We don't need to check the list's size because it can never be empty.

##### If not empty**:**

```ruby
ExampleType < Matter:
  Syntax:
    example = { "I could be empty!" }*
  Mapping:
    example -> String:
      if example.not-empty:
        example.0
      else:
        "I am empty!"
```

Before we access the first element of `example` we make sure with an _if-statement_ that the list is not empty or otherwise return `I am empty!` with an _else-statement_.

If we left out the _if-else-construct_ and the list was empty, an error would be trown and the parser would stop immediately.

