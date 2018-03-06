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
