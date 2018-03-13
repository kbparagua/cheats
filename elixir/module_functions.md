# Modules

```elixir
defmodule MyModule do
  def my_method do
    # body
  end
end

MyModule.my_method
```

## Private Function

```elixir
defmodule Foo do
  def public_bar do
    # body
  end
  
  defp private_baz do
    # body
  end
end

Foo.public_bar
Foo.private_baz # Error
```

## Guard Clauses

Will try each clauses until a match is found.

```elixir
defmodule Math do
  def zero?(0) do
    true
  end

  def zero?(x) when is_integer(x) do
    false
  end
end
```

## Alternate Syntax

```elixir
defmodule Math do
  def zero?(0), do: true
  def zero?(x) when is_integer(x), do: false
end
```

## Function Capture

Something like function reference.

```elixir
defmodule Foo do
  def bar do
    IO.puts "Blah Blah"
  end
end

fun = &Foo.bar/0
fun.() # "Blah Blah"
is_function(fun) # true
```

## Function Creation Shortcut
```elixir
fun = &(&1 + 1)
fun.(2) # 3
```

`&1` - represents 1st argument.

code above is similar to:
```elixir
fun = fn x -> x + 1 end
```
