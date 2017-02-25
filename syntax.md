# Syntax Definition

Here is a short description of each symbol or operation and what it does:



### Definition

```
header = ...
```

**Symbol:** Equals sign \(`=`\)

**Operation: **The definitions on the right side are assigned to variable on left side \(in the example above this is `header` \).

---

### Concatenation {#concatenation}

```
example = "Hello world" "!"
```

**Symbol:** Whitespace

**Operation: **The part on which the whitespace follows must be successfully parsed first. Then the part behind the whitespace must be parsed correctly, too. In the example above this means the string `Hello world` is expected first then `!` must immediately follow. So `Hello world!` would be parsed successfully while for example `Hello world !` would **not**.

---

### Alternation

```
example = "Hello world" "!" | "."
```

**Symbol:** TODO: add name \(`|`\)

**Operation: **The first part or the second is expected. In the example above this means the string `Hello world` is expected first then `!` or `.` can follow. So both `Hello world!` and `Hello world.`would be accept while for example `Hello world?` would **not**. To make an alternation better visible consider using grouping.

---

### Option

```
example = "Hello world" [ "!" ]
```

**Symbol:** Square brackets \(`[` and `]`\)

**Operation: **The part between the square brackets can exist but doesn't have to. In the example above this means the string `Hello world` is expected first then `!` can immediately follow. So `Hello world` and `Hello world!` are both valid.

