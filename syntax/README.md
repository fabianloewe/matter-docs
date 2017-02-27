# Syntax

The `Syntax` part defines rules which tell the parser what to expect from the input source.

It follows directly after the definition of the new type itself:

```ruby
ForLoop < Statement:
  Syntax:
    # Defines some rules
```

As a built-in type it has special rules. For example you can only define or declare variables here \(which are different things in Matter\). Also an assignment might look a bit different then you know from other languages. Don't worry, all this stuff will be explained in the next chapters. Let's dive into it!

