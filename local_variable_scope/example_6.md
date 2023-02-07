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

The local variable `arr` is initialized and assigned to the Array literal `[1, 2, 3, 4]` on line 4. The local variable `counter` is initialized and assigned to the Integer `0` on line 5. The local variable `sum` is initialized and assigned to the Integer `0` on line 6.

The `do...end` alongside the `loop` invocation method on lines 8-12 defines a block and introduces a new scope; within which; `sum` adds its initialized value; `0`; to the value of each`arr` index and reassigns the value back to `sum` on line 9. Each array index is accessed with the expression `arr[counter]` which starts at Integer `0` and increments by `1` on the following iterations.

`counter` adds its initialized value to the Integer `1` on each iteration and reassigns the value back to `counter`. The `break` condition on line 11 shows the loop will end once `counter` is equal to the size of the `arr`; which is the Integer `4`. The `loop` method returns `nil`.

The `puts` method is called on line 14 with a String passed to it as an argument; since the String uses interpolation for `sum`; the output is `"Your total is 10"`. `sum` is the sum of all the `arr` elements added together.

This problem demonstrates local variable scope rules in Ruby; A `loop` method with a `do...end` block passed to it as an argument introduces a new scope. When variables are initialized from outside of the block; the variables can be accessed from within the block. However, variables that are initialized from inside the block; are not accessible from outside of the block.

