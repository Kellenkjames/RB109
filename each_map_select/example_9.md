**What does the following code return? What does it output? Why? What concept does it demonstrate?**

```ruby
arr = [1, 2, 3, 4, 5, 6, 7, 8, 9, 10]

new_array = arr.map do |n|
  n > 1
  puts n
end

p new_array
```
# Written Response:

The local variable `arr` is initialized and assigned to the Array `[1, 2, 3, 4, 5, 6, 7, 8, 9, 10]` on line 4. The local variable `new_array` is initialized and assigned to the `map` method invocation on `arr`.

The `do...end` alongside the `map` method invocation defines a block on lines 6-9. Within the block; the parameter `n` represents the current element of `arr`. The expression `n > 1` is evaluated for each `n` in `arr`; this returns a new Array of boolean objects; `[false, true, true, true, true, true, true, true, true, true]`.

The `puts` method invocation passes in the reference of `n` as an argument; this outputs each Array element `[false, true, true, true, true, true, true, true, true, true]` on a newline and returns `nil` on line 8.

The `p` method invocation passes in the reference `new_array` as an argument; this outputs and returns the Array element `[false, true, true, true, true, true, true, true, true, true]`.

This problem demonstrates behaviors of `map`. The `map` method calls the block on each element and returns a new Array whose elements are the return values of the block.