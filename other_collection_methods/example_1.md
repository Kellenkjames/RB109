**What does the following code return? What does it output? Why? What concept does it demonstrate?**

```ruby
[1, 2, 3].any? do |num| 
  num > 2
end
```
# Written Response:

The `any` method invocation is called on the Array literal `[1, 2, 3]` on line 4.

The `do...end` alongside the `any?` method invocation on lines 4-6 defines a block. The parameter `num` represents the current element of the Array `[1, 2, 3]`. Within the block; the expression `num > 2` is called on each element; this returns the boolean `true` if any `num` evaluates as true; `false` otherwise.

The third element of the Array `[1, 2, 3]` evaluates as true; therefore; the return value of the method is the boolean `true`.

This problem demonstrates the behavior or the `any?` method. The `any?` method will iterate over each element in the collection and return the boolean `true` if any element in the collection evaluates as true, `false` otherwise.

