# Big O Notation

## O(1)

- Execution time is constant regardless of input size.

```ruby
def first_is_nil?(input)
  input.first.nil?
end
```

## O(N)

- Execution time is directly proportional to the input size.

```ruby
def has_nil?(input)
  input.each do |element|
    return true if element.nil?
  end
  
  false
end
```

## O(N^2)

- Execution time is directly proportional to the square of the input size.
- Common with nested iterations.

```ruby
def has_duplicate?(input)
  input.each_with_index do |element, i|
    input.each do |possible_duplicate, k|
      next if i == k
      return true if element == possible_duplicate
    end
  end
  
  false
end
```

## O(2^N)

## O(log N)
