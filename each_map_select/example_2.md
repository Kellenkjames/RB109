**What does the following code return? What does it output? Why? What concept does it demonstrate?**

```ruby
arr = [1, 2, 3, 4, 5, 6, 7, 8, 9, 10]
arr.select { |n| n.odd? }
```
# Written Response:

The local variable `arr` is initialized and assigned to the Array `[1, 2, 3, 4, 5, 6, 7, 8, 9, 10]` on line 4. The `select` method is invoked on the reference of `arr` on line 5.

The `{}` alongside the `select` method invocation defines a block on line 5. Within the block, the parameter `n` represents the current element of `arr` and the block is called on each `n` in `arr`. Each iteration will check if `n` is odd and return a new Array of elements that evaluate as truthy; therefore; the method returns the Array `[1, 3, 5, 7, 9]`.

This problem demonstrates behaviors of the `select` method. The `select` method will call the block on each element of the Array and return a new Array based on the elements that evaluate as truthy.