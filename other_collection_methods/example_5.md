**What does the following code return? What does it output? Why? What concept does it demonstrate?**

```ruby
[1, 2, 3].each_with_index do |num, index|
  puts "The index of #{num} is #{index}."
end
```
# Written Response:

The `each_with_index` method invocation is called on the Array literal `[1, 2, 3]` on line 4.

The `do...end` alongside the `each_with_index` method invocation defines a block on lines 4-6. The block parameters `num` and `index` represent the current element and index of each object in the Array literal `[1, 2, 3]'`;

Within the block; the `puts` method invocation passes in a String as an argument while using interpolation to pass in the reference of `num` and `index` for each element in the Array. This outputs each String in the Array literal `[1, 2, 3]` on a newline.

The index of `1` is `0`.
The index of `2` is `1`.
The index of `3` is `2`.

The return value of `each_with_index` method is `[1, 2, 3]`.

This problem demonstrates the behavior of the `each_with_index` method. The `each_with_index` method iterates over the collection and calls the block for each element; the return value is the calling object.