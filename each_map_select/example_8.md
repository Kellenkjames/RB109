**What does the following code return? What does it output? Why? What concept does it demonstrate?**

```ruby
arr = [1, 2, 3, 4, 5, 6, 7, 8, 9, 10]

new_array = arr.map do |n|
  n > 1
end

p new_array
```
# Written Response:

The local variable `arr` is initialized and assigned to the Array `[1, 2, 3, 4, 5, 6, 7, 8, 9, 10]` on line 4. The local variable `new_array` is initialized and assigned to calling the `map` method on `arr`. The `do...end` alongside the `map` method defines a block on lines 6-8; the parameter `n` represents the current element of `arr`.

Within the block; the expression `n > 1` is evaluated for each element; since this expression checks for truthiness; the method will return a new array of boolean objects; `[false, true, true, true, true, true, true, true, true, true]`.

The `p` method is called with `new_array` passed to it as an argument; the output is `[false, true, true, true, true, true, true, true, true, true]` and the return value is the same.

This problem demonstrates the behaviors of the `map` method. `map` calls the block with each element of `self` and returns a *new* Array whose elements are the return values from the block; this will not affect the original object.