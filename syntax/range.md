# Range

A _range_ is rule which expects one or more characters in a certain range. Basically this rule type is just syntactic sugar to prevent huge [alternations](//syntax/alternation.md). Currently you can only specify a range of the following characters:

* Lowercase letter to lowercase letter \(`a` to `z`\)
* Uppercase letter to uppercase letter \(`A` to `Z`\)
* Digit to digit \(`0` to `9`\)

Ranges of multiple characters are allowed as long as they consist of one of the above kinds. These ranges are evaluated \(like decimal numbers are incremented\) from right to left. To get a better understanding of this see the example below.

### Example

```ruby
example = "aaa".."azz"
```

Any word between `aaa` and `azz` is allowed. You could rewrite this example like this:

```ruby
example = "aaa" | "aab" | "aac" | ... | "ayz" | "azz"
```

This outlines very well how the most right character is iterated first, then the one left before it and so on.

**Valid strings:** `abc` , `ayz`

**Invalid strings:**`bbb`, `bzz`

