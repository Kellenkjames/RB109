**What does the following code return? What does it output? Why? What concept does it demonstrate?**

```ruby
[1, 2, 3].any? do |num| 
  num > 2
end
```
# Written Response:

The `do...end` alongside the `any?` method on lines 4-6 defines a block; while the parameter `num` represents the current element of the Array `[1, 2, 3]`. Within the block; the expression `num > 2` is called for each element; returns `true` if the block returns any truthy value, `false` otherwise. 

The third element of the Array `[1, 2 , 3]` evaluates as truthy; therefore; the return value of the method is `true`.

This problem demonstrates the behavior or the `any?` method. The `any?` method will iterate over each element in the collection, however; it will not return an object of the same type as the calling object; i.e., Array; it returns a boolean value; `true` or `false`.

