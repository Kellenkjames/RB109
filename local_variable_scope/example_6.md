**What does the following code return? What does it output? Why? What concept does it demonstrate?**

```ruby
arr = [1, 2, 3, 4]
counter = 0
sum = 0

loop do
  sum += arr[counter]
  counter += 1
  break if counter == arr.size
end

puts "Your total is #{sum}"
```

# Written Response:

On line 4, the local variable `arr` is initialized and assigned to the array `[1, 2, 3, 4]`.
On line 5, the local variable `counter` is initialized and assigned to the integer `0`.
On line 6, the local variable `sum` is initialized and assigned to the integer `0`.

The `do...end` alongside the `loop` method invocation on lines 8-12 defines a block and introduces a new scope. On line 9, `sum` uses the shorthand operator to add its initial value; `0`, to each `arr` element and re-assigns the total back to `sum`.

On line 10, `counter` uses the shorthand operator to add its initial value; `0`, to `1` on each iteration of the loop and re-assigns the total back to `counter`. On line 11, the `loop` will break after `4` iterations; same count as the size of `arr`. The `loop` method returns `nil`.

On line 14, we invoke the `puts` method and pass a string in as an argument. The output is: `"Your total is 10"` and the `puts` method returns nil.

This problem demonstrates variable local scoping rules. From inside the block, you can access variables that were initialized outside the block; in this case; we have access to `arr`, `counter`, and `sum` inside the block.


