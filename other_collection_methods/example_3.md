**What does the following code return? What does it output? Why? What concept does it demonstrate?**

```ruby
[1, 2, 3].all? do |num|
  num > 2
end
```
# Written Response:

The `all` method invocation is called on the Array literal `[1, 2, 3]` on line 4.

The `do...end` alongside the `all?` method invocation defines a block on lines 4-6; the `num` parameter represents the current element of the Array literal `[1, 2, 3]`. Within the block; the expression `num > 2` is called on each element. Since `num > 2` doesn't evaluate as true for every `num` in the Array literal `[1, 2, 3]`, the return value is the boolean `false`.

This problem demonstrates the behavior of the `all?` method. The `all?` method will iterate over the collection and call the block on each element. The method will return the boolean `true` if every element in the collection evaluates as true; `false` otherwise.