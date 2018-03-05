# Conditions

## `if` and `unless`
```elixir
if true do
  "Orayt!"
else
  "Shhit"  
end
```

### Alternate Syntax
```elixir
if true, do: "Orayt!", else: "Shhit"
```

## `case`

```elixir
case value do
  pattern_1 -> "Do this"
  pattern_2 -> "Or this"
  _ -> "else do this shit"
end
```

Example:
```elixir
case {1, 2, 3} do
  {:a, :b, :c} -> "This will not match!"
  {x, 2, 3} -> "This will match! and x will be binded to #{x}"
  _ -> "This will not match too"
end

# "This will match! and x will be bineded to 1"
```

### Guards
- add extra condition to patterns.

```elixir
case value do
  pattern when expression -> # do this 
end
```

Example:
```elixir
case {:ok, "Hello World"} do
  {status, content} when status == :ok ->
    "Success!"
  _ ->
    "Failed!"
end
# "Success!"
```

### Errors
- Error will be raised when no pattern is matched.
- Error on guard clause will silently fail.
```elixir
case {:ok, "Hello"} do
  {status, content} when xyz > yzz -> # This will not raise an error even if variable is invalid.
    "Success!"
  _ ->
    "Failed"
end
# Failed
```
