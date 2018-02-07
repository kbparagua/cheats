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
## Output

```elixir
IO.puts "Hello World"
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

## Identifying Functions

Name + Arity *(number of arguments)*. Example: `div/2`

## Type Checking

`is_<type>/1`.

Types:
- `boolean`
- `integer`
- `float`
- `number` (float or integer)
- `atom`
- `list`
- `tuple`

Example:
```elixir
is_boolean(true) # true
```

## Strings

Interpolation
```elixir
"Hello #{:world}" # Hello world
```

### String functions

```elixir
String.length "Hello" # 5
String.upcase "hello" # "HELLO"
```
