**What does the following code return? What does it output? Why? What concept does it demonstrate?**

```ruby
arr = [1, 2, 3, 4, 5, 6, 7, 8, 9, 10]
arr.select { |n| n.odd? }
```
The local variable `arr` is initialized and assigned to the Array `[1, 2, 3, 4, 5, 6, 7, 8, 9, 10]` on line 4.

The `{}` alongside the `select` method defines a block on line 5. Within the block, the parameter `n` represents the current element of `arr` and the expression `n.odd?` is evaluated for each element in `arr`; the block is passed to the `select` method as an argument.

The `select` method returns a new Array; `[1, 3, 5, 7, 9]`.

This problem demonstrates the behaviors of the `select` method. The `select` method will select all elements that evaluate as truthy and return a *new* array; it does not mutate the original object.

