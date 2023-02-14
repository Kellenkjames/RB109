**What does the following code return? What does it output? Why? What concept does it demonstrate?**

```ruby
arr = [1, 2, 3, 4, 5, 6, 7, 8, 9, 10]

incremented = arr.map do |n|
  n + 1
end

p incremented
```
# Written Response:

The local variable `arr` is initialized and assigned to the Array `[1, 2, 3, 4, 5, 6, 7, 8, 9, 10]` on line 6. The local variable `incremented` is initialized and assigned to the `map` method invocation being called on `arr`.

The `do...end` alongside the `map` method invocation defines a block on lines 6-8; Within the block; the parameter `n` represents each element in`arr`. The expression `n + 1` will be evaluated for each `n` in `arr`. Since `map` calls the block for each `n` and returns a new value for each `n`; it will return a new Array of elements; `[2, 3, 4, 5, 6, 7, 8, 9, 10, 11]`.

The `p` method invocation passes in the reference of `incremented` as an argument on line 10; this outputs the Array `[2, 3, 4, 5, 6, 7, 8, 9, 10, 11]` and returns the same object.

This problem demonstrates behaviors of the `map` method. The `map` method will call the block on each element and returns a new Array whose elements are the return values from the block.