**What does the following code return? What does it output? Why? What concept does it demonstrate?**

```ruby
{ a: "ant", b: "bear", c: "cat" }.each_with_object({}) do |(key, value), hash|
  hash[value] = key
end
```
# Written Response:

The `do...end` alongside the `each_with_object` on lines 4-6 defines a block; the `each_with_object` method is called and passes an empty Hash to it as an argument. The block parameters `(key, value)` represents the current key-value pair of the calling object; `{"ant"=>:a, "bear"=>:b, "cat"=>:c}`; the block parameter `hash` represents the argument passed to the `each_with_object` method; an empty Hash.

Within the block; the expression `hash[value] = key` will take each current element's and reverse the order of the association; for example, the value becomes the key and the key becomes the return value is `{"ant"=>:a, "bear"=>:b, "cat"=>:c}`.

This problem demonstrates the behavior of the `each_with_object` method. The `each_with_object` method accepts an object as the argument that is passed to it; this is the return value of the method. The argument can be either of the same object type or different; the original object is left unchanged.

