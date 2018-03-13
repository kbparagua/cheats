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
