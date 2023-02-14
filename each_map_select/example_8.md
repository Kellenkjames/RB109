**What does the following code return? What does it output? Why? What concept does it demonstrate?**

```ruby
arr = [1, 2, 3, 4, 5, 6, 7, 8, 9, 10]

new_array = arr.map do |n|
  n > 1
end

p new_array
```
# Written Response:

The local variable `arr` is initialized and assigned to the Array `[1, 2, 3, 4, 5, 6, 7, 8, 9, 10]` on line 4. The local variable `new_array` is initialized and assigned to the `map` method invocation on `arr`.

The `do...end` alongside the `map` method defines a block on lines 6-8. Within the block; the parameter `n` represents the current element of `arr`. The expression `n > 1` is evaluated for each `n` in `arr`; Since this expression evaluates for truthiness; the `map` method will return the Array `[false, true, true, true, true, true, true, true, true, true]`.

The `p` method invocation passes in the reference of `new_array` as an argument on line 10; the output is the Array `[false, true, true, true, true, true, true, true, true, true]` and the return value is the same object.

This problem demonstrates the behaviors of the `map` method. `map` calls the block with each element of `self` and returns a new Array whose elements are the return values from the block.