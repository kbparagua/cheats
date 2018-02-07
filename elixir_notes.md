# Elixir Notes

## Basic Data Types
```elixir
1         # integer
1.0       # float
true      # boolean
:atom     # atom / symbol
[1, 2, 3] # list
{1, 2, 3} # tuple
```

## Basic Arithmetic

`/` always returns a float.
```elixir
10 / 2 # 5.0
```

`div/2` for integer result.
```elixir
div(10, 2) # 5
```

`rem/2` to get division remainder.
```elixir
rem(10, 3) # 1
```

`round/1` to get closes integer.
```elixir
round(3.58) # 4
```

`trunc/1` to get integer part of float.
```elixir
trunc(3.58) # 3
```
