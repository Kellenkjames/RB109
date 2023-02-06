**What does the following code return? What does it output? Why? What concept does it demonstrate?**

```ruby
[1, 2, 3].all? do |num|
  num > 2
end
```
# Written Response:

The `do...end` alongside the `all?` method defines a block on lines 4-6; the `num` parameter represents the current element of the Array `[1, 2, 3]`. Within the block; the expression `num > 2` is called for each element. The `all?` method returns `true` if all elements of `self` meet a given criterion; in this example; the criterion is not met for each element; therefore; the return value is `false`.

This problem demonstrates the behavior of the `all?` method. The `all?` method will iterate over each element and evaluate the given expression for each element; it will not return an object of the same type as the caller; it will return a boolean; `true` or `false`.



