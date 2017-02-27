## Declaration

A _declaration_ specifies an un-assigned variable of certain type. This means any type that is derived from this one, **must** assign a rule to that variable or the compiler will throw an error. The naming convention for the variable's name are the same like for a [definition](//syntax/definition.md).

#### Example

```ruby
BaseType < Matter:
  Syntax:
    example: String
```

The variable `example` is expected to be a `String` rule. A valid derived type of `BaseType` would be:

```ruby
DerivedType < Matter:
  Syntax:
    example = "Hello world"
```



