# Keyword List

```elixir
list = [{:a, 1}, {:b, 2}]
```
- list is composed of 2-item tuples.
- 1st item is the key, while the 2nd is the value.
- key should be an atom.
- just like hash in other languages.

**Easier Syntax**
```elixir
list = [a: 1, b: 2]
```

## Adding Values

```elixir
list = [a: 1, b: 2]
new_list = list ++ [c: 3]
# [a: 1, b: 2, c: 3]
```

## Accessing Values

```elixir
list = [a: 1, b: 2, c: 3]
list[:a] # 1
```

ONLY the first matched key will be fetched.

```elixir
list = [a: 0, a: 100, b: 2]
list[:a] # 0
```

## Function Options

- keyword list is mainly used when passing options to functions.
- when the last argument is a list `[]` is optional.
```elixir
my_func(1, [option_1: 1, option_2: 2])
my_func(1, option_1: 1, option_2: 2)
```

# Maps
