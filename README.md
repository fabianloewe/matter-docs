# The Matter Language

### What is it for?

**In short:** Matter makes it easy to create new full grown programming languages, DSLs \(Domain Specific Language\) or grammars in general.

**More descriptive: **Matter simplifies the multiple stages of parsing, creating an AST \(Abstract Syntax Tree\) and optionally compiling source code.

### Why that name?

In this language the most basic thing you can use is "Matter". Like in our world everything is matter in the end.

### How does it look like?

Good question, we talked enough about what is. Let's get practical and start by creating a simply foreach-loop. This is very common construct and can be found in programming languages like C++ or Java. Here is an example how this statement looks like in Java:

```java
for(int i : arrayOfInts) {
    // do something
}
```

Great, but how can we parse this in Matter? Here we go:

```ruby
ForLoop < Statement:
  Syntax:
    header = "for" element ":" collection
    element = Type Variable
    collection = Variable
    body = "{" newline statements newline "}" 
    statements = { Statement }*
```

Do you understand what we did here? You have heared about [EBNF \(Extended Backus-Naur Form\)](https://en.wikipedia.org/wiki/Extended_Backus%E2%80%93Naur_form "EBNF description on Wikipedia")?

Not? Don't worry, you can move on to the next chapter describing this syntax: [Syntax Definition](///syntax.md#syntax-definition).

You have? Impressive! Then you likely found some differences between what you know and what this code looks like. Here are all differences described:

* **Concatenation: **No comma \(`,`\) needed! A whitespace concatenates two definitions.
* **Termination:** No semicolon \(`;`\) needed! Each line is one definition. To define multiple things just use multiple variables.
* **Terminal strings: **Always use double quotes \(`"`\)! Single quotes \(`'`\) are **not** **allowed**!
* **Special sequences: **Do not exist! Everything must be defined somewhere.
* **Ranges:** Matter has a range operation: two dots \(`..`\). More about that here.



