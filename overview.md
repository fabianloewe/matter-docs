# Overview

Before we can start coding, we need to have target that we want to parse. A common and quite simple language construct is the _for-each loop_ and can be found in programming languages like C++ \(since C++11\) or Java. Here is an example how this statement looks like in Java:

```java
for(int i : arrayOfInts) {
    // do something
}
```

Now comes the interesting part: How can we describe this statement in Matter? Below is an answer:

```ruby
ForLoop < Statement:
  Syntax:
    header = "for" element ":" collection
    element = Type Variable
    collection = Variable
    body = "{" newline statements newline "}" 
    statements = { Statement }*
```

On the first look you might feel a bit irritated. In the next parts we will discover everything we see here. So let's move on!

