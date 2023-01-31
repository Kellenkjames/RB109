**What does the following code return? What does it output? Why? What concept does it demonstrate?**

```ruby
a = 4

loop do
  a = 5
  b = 3

  break
end

puts a
puts b
```

# Written Response:

On line 4, the local variable `a` is initialized and assigned to the integer `4`. The `do...end` alongside the `loop` method invocation on lines 6-11 defines a block and introduces a new scope. On line 7 `a` is re-assigned to the integer `5`.  On line 8, `b` is initialized and assigned to the integer `3`. The return value of the `loop` method is nil.

On line 13, we invoke the `puts` method and pass in `a` as an argument. Since `a` was re-assigned to the integer `5` inside the block and `a` was initialized outside of the block; `5` is the output and the return value is `nil`.

On line 14, we invoke the `puts` method and pass in `b` as an argument. Since `b` was initialized from inside the block, this is the output: `undefined local variable or method 'b' for main:Object`. This means `b` is not accessible anywhere outside of the block since it was initialized from inside the block. 

This problem demonstrates variable local scoping rules. From inside the block, you can access variables that were initialized outside of the block. However, from outside of the block, you can't access any variables that were initialized inside the block. 

