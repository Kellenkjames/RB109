**What does the following code return? What does it output? Why? What concept does it demonstrate?**

```ruby
{ a: "ant", b: "bear", c: "cat" }.each_with_object([]) do |pair, array|
  array << pair.last
end
```
# Written Response:

The `do...end` alongside the `each_with_object` method defines a block on lines 4-6; the `each_with_object` is called on the Hash literal `{ a: "ant", b: "bear", c: "cat" }` and passes in an empty Array to it as an argument; The block parameter `pair` represents the current key value pair of the Hash literal `{ a: "ant", b: "bear", c: "cat" }`; while the block parameter `array` represents the argument passed to the `each_with_object` method; an empty Array.

Within the block; the expression `array << pair.last` will push the last value of each `pair` into the `array`. The method returns the following Array: `["ant", "bear", "cat"]`.

This problem demonstrates the behavior of the `each_with_object` method. The `each_with_object` method is called on a object; i.e., `Hash`, and passes in a different object type, i.e., `Array`, as an argument to the method. The block is called on each element and the method returns a new object with the return values from the block. The argument that is passed into the `each_with_object` is the object that is returned; leaving the calling object unchanged.

