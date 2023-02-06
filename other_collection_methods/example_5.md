**What does the following code return? What does it output? Why? What concept does it demonstrate?**

```ruby
[1, 2, 3].each_with_index do |num, index|
  puts "The index of #{num} is #{index}."
end
```
# Written Response:

The `do...end` alongside the `each_with_index` method defines a block on lines 4-6; the block parameters `num` and `index` represent the current element and index of each object in Array `[1, 2, 3]'`;

Within the block; the `puts` method is called with a String passed to it as an argument. The String argument uses interpolation for the `num` and `index` and outputs the following:

The index of `1` is `0`.
The index of `2` is `1`.
The index of `3` is `2`.

The return value of the `each_with_index` method is `[1, 2, 3]`.

This problem demonstrates the behavior of the `each_with_index` method. The `each_with_index` method iterates over array indexes and returns the calling object; no matter what expressions are called on elements from inside the block. 

