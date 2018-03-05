# Operators

## Logical
### `and`, `or`, `not`
- first argument MUST be boolean (`true` or `false`)
- raises an exception if first arg is not boolean.
```
1 and true
# ERROR!
```

### `&&`, `||`, `!`
- not strcit; can pass non-boolean values.
- everything is true except `false` and `nil`.

## Comparison

### `==` vs `===`

`===` is more strict when comparing integer and floats.
```
1 == 1.0 # true
1 === 1.0 # false
```

### Comparing Different Types
No need to memorize this shit.
`number < atom < reference < function < port < pid < tuple < map < list < bitstring`
