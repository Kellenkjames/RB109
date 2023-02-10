**What does the following code return? What does it output? Why? What concept does it demonstrate?**

```ruby
a = "hello"
[1, 2, 3].map { |num| a}
```
# Written Response:

The local variable `a` is initialized and assigned to the String `"hello"` on line 4. The `map` method is called on `[1, 2, 3]` on line 5. The `{}` alongside the `map` method defines a block and introduces a new scope. Within the block; the parameter `num` represents each element in `arr`. 

Since `a` was initialized in the outer scope; the String `"hello"` is passed to the block for each `num`; this returns a new Array; `["hello", "hello", "hello"]`.

This problem demonstrates behaviors of the `map` method and local variable scope. When a variable is initialized from outside of a block; the variable is accessible inside of the block. The `map` method doesn't always perform transformation on elements; sometimes; it simply returns the same element in a new Array.


