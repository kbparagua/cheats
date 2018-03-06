# Keyword List

```elixir
list = [{:a, 1}, {:b, 2}]
```
- list is composed of 2-item tuples.
- 1st item is the key, while the 2nd is the value.
- key should be an atom.
- order is defined by the programmer.
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
- key-value data structure just like keyword list.
- keys can be anything (unlike keyword list which requires an atom).
- no ordering.

```elixir
map = %{:one => 1, 2 => :two}
```

## Accessing Values
```elixir
map = %{:one => 1, 2 => :two}
map[:one] # 1
map[2] # :two
map[:fuck] # nil
```

Another syntax if key is an atom.
```elixir
map = %{:one => 1, 2 => :two}
map.one # 1
```

## Updating Values
```elixir
map = %{:one => 1, 2 => :two}
%{map | 2 => "TWO"} # %{:one => 1, 2 => "TWO"}
```
This will fail if the given key is not existing.

## Pattern Matching
- will always match on a subset of a value.

```elixir
%{} = %{:a => 1, :b => 2} # %{:a => 1, :b => 2}
%{:a => x} = %{:a => 1, :b => 2} # %{:a => 1, :b => 2}
x # 1

%{:c => 10000} = %{:a => 1, :b => 2} # Error!
```

## Easier Syntax

When all keys are atoms.

```elixir
map = %{a: 1, b: 2}
```


# Nested Structure

```elixir
users = [
  bob: %{age: 5},
  alice: %{age: 10}
]

users[:bob].age # 5
```

## Updating Value

```elixir
put_in users[:alice].age, 12
```
