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

The `do...end` alongside the `map` method invocation defines a block on lines 6-8; Within the block; the parameter `n` represents each element in`arr`. The block will be called on each `n`; which results in the expression `n + 1` being on called on each `n`; this returns a new Array with the return values from the block; `[2, 3, 4, 5, 6, 7, 8, 9, 10, 11]`.

The `p` method invocation passes in the reference of `incremented` as an argument on line 10; this outputs and returns the Array `[2, 3, 4, 5, 6, 7, 8, 9, 10, 11]`.

This problem demonstrates behaviors of the `map` method. The `map` method will call the block on each element and returns a new Array whose elements are the return values from the block.