# Lists

`[1, 2, 3, 4, 5]`

## Length

```
length [1, 2, 3] # 3
```

## Concatenation
```
[:x, :y, :z] ++ [:a, :b]
# [:x, :y:, :z, :a, :b]
```

## Subtraction
```
[:x, :y, :z, :y] -- [:y]
# [:x, :z, :y]
```

## Head
```
list = [1, 2, 3]
hd list # 1
```

## Tail
Contents of the list without the head.
```
list = [1, 2, 3]
tl list # [2, 3]
```

Error when getting head/tail of empty list.
```
hd [] # Argument Error
tl [] # Argument Error
```
