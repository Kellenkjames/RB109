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

The local variable `arr` is initialized and assigned to the Array literal `[1, 2, 3, 4]` on line 4. The local variable `counter` is initialized and assigned to the Integer literal `0` on line 5. The local variable `sum` is initialized and assigned to the Integer literal `0` on line 6.

The `do...end` alongside the `loop` method invocation on lines 8-12 defines a block and introduces a new scope; within which; `sum` adds its initialized value; the Integer literal `0` to the value of each `arr` index and reassigns the total back to `sum`; on line 9. Each array index is accessed with the expression `arr[counter]` which begins at Integer literal `0` and increments by the Integer literal `1` on each new iteration.

`counter` adds its initialized value; the Integer literal `0`; to the Integer literal `1` on each iteration and reassigns the value back to `counter`. The `break` condition shows the loop will end once `counter` is equal to the size of the `arr` on line 11; The `arr` size is equivalent to the Integer literal `4`; therefore; the `loop` method will iterate the Integer literal `4` times before stopping. The `loop` method invocation returns `nil`.

The `puts` method invocation passes a String reference to it as an argument on line 14. Since the String uses interpolation for `sum`; the output is `"Your total is 10"`. `sum` is the sum of all `arr` elements added together; which is the Integer literal `10`.

This example demonstrates local variable scoping rules in Ruby; when a block is passed to a `loop` method invocation; it introduce a new scope. From inside the block, you can access variables that were initialized outside of the block. However, from outside the bock, you can't access any variables that were initialized inside the block.

