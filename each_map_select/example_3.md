**What does the following code return? What does it output? Why? What concept does it demonstrate?**

```ruby
arr = [1, 2, 3, 4, 5, 6, 7, 8, 9, 10]

new_array = arr.select do |n|
  n + 1
end

p new_array
```

The local variable `arr` is initialized and assigned to the Array `[1, 2, 3, 4, 5, 6, 7, 8, 9, 10]`.The local variable `new_arr` is initialized and assigned to calling the `select` method on `arr` while passing the `do...end` to it as a block.

The `do...end` alongside the `select` method on lines 6-8 defines a block; the parameter `n` represents the current element of `arr`. On line 7, within the block; the expression `n + 1` is evaluated for each element in `arr` and the block is passed to the `select` method as an argument.

`new_array` returns the original object; `[1, 2, 3, 4, 5, 6, 7, 8, 9, 10]`.

The `p` method is called on line 10 and `new_array` is passed to it as an argument; the output is the original object `[1, 2, 3, 4, 5, 6, 7, 8, 9, 10]`; printed on a single line; the return value is the same object.

This problem demonstrates the behaviors of the `select` method. The `select` method always evaluates a given block based on truthiness. In this case, a math operation on each element has no effect as the method does not perform transformations (like with map); therefore; the original object is returned.


