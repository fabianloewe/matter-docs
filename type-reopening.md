# Matter reopening

Again something Ruby uses, too. Reopening a matter allows to add definitions or override existing ones.

This happens in the second line:

```ruby
ForLoop < Statement:
  Syntax:  # Reopen Syntax
    ...    # New stuff for Syntax
```

As a difference to Ruby, in Matter it is clear if a matter type is reopened or newly defined. A matter name followed by a colon \(`:`\) always means the matter type must already be defined somewhere. In our example [`Syntax`](//syntax/README.md) is a built-in type from inside of `Matter` which is the incredible base thing of everything and defined by the compiler \(so built-in, too\).

Because our ancestor `Statement` is a descendant of `Matter` it also has [`Syntax`](//syntax/README.md) defined and thus it can be reopened in any other descendant of it. Sounds a bit compilcated? Here comes another example:

```ruby
SomeType < Matter:     # Matter = base type
  ChildType < Matter:  # A child type
    var1 = 1           # An exemplary variable

OtherType < SomeType:  # OtherType derives from SomeType
  ChildType:           # Reopened
    var1 = 2           # Overriden
    var2 = 3           # New variable defined
```

This example shows what a _child_ and _parent_ is in Matter:

* `ChildType` is a _child_ of `SomeType` \(because it is defined "inside" it\).
* `SomeType` is the _parent_ of `ChildType` \(it is defined "above" it\).

Children are copied as they are from the perspective of the ancestor to its descendants. The exemplary variable `var1` of matter `ChildType` in parent `OtherType` would have a value of `2` in all descendants of `OtherType` unless they override the variable again.

