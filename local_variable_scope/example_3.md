**What does the following code return? What does it output? Why? What concept does it demonstrate?**

```ruby
a = 4
b = 2

loop do
  c = 3
  a = c
  break
end

puts a
puts b
```

# Written Response:

On line 4, the local variable `a` is initialized and assigned to the integer `4`.
On line 5, the local variable `b` is initialized and assigned to the integer `2`.

The `do...end` alongside the `loop` method invocation on lines 7-11 defines a block and introduces a new scope. On line 8, the local variable `c` is initialized and assigned to the integer `3`. On line 9, `a` is re-assigned to `c`. The `loop` method returns `nil`.

On line 13, we invoke the `puts` method and pass in `a` in as an argument. Since `a` is re-assigned to `c` on line 9 and `c` was assigned to the integer `3` on line 8; the output is `3`. The method returns `nil`.

On line 14, we invoke the `puts` method and pass in `b` in as an argument. The output is the integer `2`; same as the initialization value on line 2.

This problem demonstrates variable local scoping rules. From inside the block, you can access variables that were initialized outside of the block.






