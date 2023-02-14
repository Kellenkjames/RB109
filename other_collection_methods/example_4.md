**What does the following code return? What does it output? Why? What concept does it demonstrate?**

```ruby
{ a: "ant", b: "bear", c: "cat" }.all? do |key, value|
  value.length >= 3
end
```
# Written Response:

The `all?` method invocation is called on the Hash literal `{ a: "ant", b: "bear", c: "cat" }` on line 4.

The `do...end` alongside the `all?` method invocation defines a block from lines 4-6. The block parameters `key` and `value` represent the current key-value pair of each element within the Hash literal `{a: "ant", b: "bear", c: "cat" }`. Within the block; the expression `value.length >= 3` is called on each `key` and `value` within the Hash literal `{ a: "ant", b: "bear", c: "cat" }`.

The `all?` method returns the boolean `true` when the block is called on each element and each element evaluates as true. Since every `value` of the Hash literal `{ a: "ant", b: "bear", c: "cat" }` evaluates as true, the method returns the boolean `true`.

This method demonstrates the behaviors of the `all?` method. `all?` iterates over each element in the collection and evaluates against the given expression; it does not return an object of the same type as the caller; it returns a boolean; `true` or `false`.