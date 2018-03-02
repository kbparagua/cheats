# Pattern Matching

`a = 1 # 1` - this is NOT an assignment statement! This is a match statement! Wat!?

- `a` - pattern or term
- `1` - expression

so this is valid:
`1 = a # 1`

because the pattern `1` is equal to the expression `a` *(has a value of 1)*.

If there is a variable on the pattern, any matching element on the right side will be binded to that variable.
Since `a` is a variable, and it matched `1`, then `a` is binded to the value `1`.

Example using a list.
```
[a, b, c] = [1, 2, 3]
a # 1
b # 2
c # 3
```

Will raise an error if there is no match. Like:
```
[a, b, c] = [1, 2]
# This will not match since I have 3 elements on the pattern side, and only 2 element on the expression side.
```

Values or constants are also allowed on the pattern side.
```
[1, other] = [1, "hello"]
other # "hello"
```

Again, only the variable on the pattern side will be binded to a value.

If a value/constant doesn't match, then it will raise an error.
```
["YES", word] = ["NO", "Shit"]
# This will not match since the expression side's first element should be "YES"
```
## Underscore

Use the special variable `_` if you do not care about a specific value in a pattern.

```
[x, y, _] = [1, 2, "Garbage shit"]
x # 1
y # 2
_ # Error! You cannot read this shit.
```

## Pin Operator
To use the variable's value in the pattern side, use the pin operator `^`.
```
x = 1
[^x, y] = [1, 2]
x # 1
y # 2

# This is basically just the same as typing
[1, y] = [1, 2]
```
