**What does the following code return? What does it output? Why? What concept does it demonstrate?**

```ruby
{ a: "ant", b: "bear", c: "cat" }.each_with_object({}) do |(key, value), hash|
  hash[value] = key
end
```
# Written Response:

The `do...end` alongside the `each_with_object` on lines 4-6 defines a block; the `each_with_object` method is called on the Hash literal `{ a: "ant", b: "bear", c: "cat" }` and passes an empty Hash to it as an argument. The block parameters `(key, value)` represents the current key value pair of the calling object; `{"ant"=>:a, "bear"=>:b, "cat"=>:c}`; the block parameter `hash` represents the argument passed to the `each_with_object` method; an empty Hash.

Within the block; the expression `hash[value] = key` will take the current element key value pair and reverse the order of the association; for example, the value becomes the key and the key becomes the return value is `{"ant"=>:a, "bear"=>:b, "cat"=>:c}`.

This problem demonstrates the behavior of the `each_with_object` method. The `each_with_object` method is called on a object; i.e., `Hash`, and passes in a different object type, i.e., `Array`, as an argument to the method. The block is called on each element and the method returns a new object with the return values from the block. The argument that is passed into the `each_with_object` is the object that is returned; leaving the calling object unchanged.