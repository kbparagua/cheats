# Big O Notation

## O(1)

Execution time is constant regardless of input size.

```ruby
def first_is_nil?(input)
  input.first.nil?
end
```

## O(N)

Execution time is directly proportional to the input size.

```ruby
def has_nil?(input)
  input.each do |element|
    return true if element.nil?
  end
  
  false
end
```

## O(N^2)

## O(2^N)

## O(log N)
