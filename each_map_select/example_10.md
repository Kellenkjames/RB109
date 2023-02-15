**What does the following code return? What does it output? Why? What concept does it demonstrate?**

```ruby
a = "hello"
[1, 2, 3].map { |num| a }
```
# Written Response:

The local variable `a` is initialized and assigned to the String `"hello"` on line 4. The `map` method is called on the Array literal `[1, 2, 3]` on line 5.

The `{}` alongside the `map` method invocation defines a block and introduces a new scope. Within the block; the parameter `num` represents each element in the Array literal `[1, 2, 3]`. Since `a` was initialized in the outer scope; the reference of `a`; which is the String `"hello"` is called for each `num`; this returns a new Array with the return values from the block; `["hello", "hello", "hello"]`.

This problem demonstrates behaviors of the `map` method and local variable scope. When a variable is initialized from outside of a block; the variable is accessible from inside of the block. The `map` method calls the block on each element and returns a new Array whose elements are the return values of the block.


