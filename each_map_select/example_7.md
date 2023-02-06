**What does the following code return? What does it output? Why? What concept does it demonstrate?**

```ruby
arr = [1, 2, 3, 4, 5, 6, 7, 8, 9, 10]

incremented = arr.map do |n|
  n + 1
end

p incremented
```
# Written Response:

The local variable `arr` is initialized and assigned to the Array `[1, 2, 3, 4, 5, 6, 7, 8, 9, 10]` on line 6. The local variable `incremented` is initialized and assigned to calling the `map` method on `arr`. The `do...end` alongside the `map` method defines a block on lines 6-8; while the block parameter `n` represents the current element of each array. Within the block; the expression `n + 1` is evaluated on each element  After the block is passed to the `map` method for each element; the return value is a new array; `[2, 3, 4, 5, 6, 7, 8, 9, 10, 11]`.

The `p` method is called with `incremented` passed to it as an argument. The output is the new array; `[2, 3, 4, 5, 6, 7, 8, 9, 10, 11]`, the return value is the same object.

This problem demonstrates behaviors of the `map` method. The `map` method calls the block with each element of `self` and returns a *new* Array whose elements are the return values from the block. The original object is not affected.

