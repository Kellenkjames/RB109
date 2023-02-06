**What does the following code return? What does it output? Why? What concept does it demonstrate?**

```ruby
{ a: "ant", b: "bear", c: "cat" }.all? do |key, value|
  value.length >= 3
end
```
# Written Response:

The `do...end` alongside the `all?` method defines a block from lines 4-6. The block parameters `key` and `value` represent the current key-value pair of each element within the Hash `{a: "ant", b: "bear", c: "cat" }`. Within the block; the expression `value.length >= 3` is called on each element and evaluates for truthiness.

The `all?` method returns `true` if all elements of `self` meet a given criterion. In this case; all elements meet the given criterion; therefore; the method returns `true`.

This method demonstrates the behaviors of the `all?` method. `all?` iterates over each element in the collection and evaluates against the given expression; it does not return an object of the same type as the caller; it returns a boolean; `true` or `false`.

