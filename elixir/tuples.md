# Tuples

- Just like list but uses `{}` instead of `[]`
- store elements contiguously in memory.
- accessing element by index or getting size is fast.

```
tuple = {:ok, "hello"}
```

## Getting Element
```
tuple = {:ok, :fck}
elemt(tuple, 0) # :ok
```

## Set Element
```
tuple = {:a, :b, :c}
put_elem(tuple, 1, :B) # {:a, :B, :c}
```
- will not change the original tuple.
- will return a new tuple object.
