# Mapping

After we have defined a syntactical rules it's time to do something with them. In most compilers you will find that a parser _maps_ a successful parsing rule to an AST type. In Matter we don't map these results to new types but instead convert them to a different type.

To better understand this let's look at our example:

```ruby
ForLoop < Statement:  
  Syntax:
    header = "for" element ":" collection
    element = Type Variable
    collection = Variable
    body = "{" newline statements newline "}" 
    statements = { Statement }*

  Mapping:
    collection -> String: collection.name
```

We reopen the built-in pseudo type `Mapping` and define a conversion. Before further explaining this let's check out first how the type `Variable` looks like:

```ruby
Variable < Matter:
  Syntax:
    name = "some" "naming" "rules"
  Mapping:
    name -> String  
```

Here `Mapping` converts the rule variable `name` to a variable of type `String` with the same name. It really is so simple because syntax rules consisting of strings only can be auto-converted to variables of type `String`.

For us this means the `collection` variable contains an already converted variable named `name` which we can simply return as our conversion result.

If we would have to do more operations on `collection` we would do so this way:

```ruby
ForLoop < Statement:  
  Syntax:
    ...
  Mapping:
    collection -> String:
      name = collection.name  # Create a new variable 
      name                    # Return it
```

Beside `String` there are more types available which are introduced to you in the next parts.

