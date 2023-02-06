**What does the following code return? What does it output? Why? What concept does it demonstrate?**

```ruby
{ a: "ant", b: "bear", c: "cat" }.any? do |key, value|
  value.size > 4
end
```
# Written Assessment:

The `do...end` alongside the `any?` method defines a block on lines 4-6. The block parameters `key` and `value` represent the current key-value pair of the Hash `{ a: "ant", b: "bear", c: "cat" }`.

Within the block; the expression `value.size > 4` is called for each element. The `any?` method returns true if any element satisfies the given criterion; `false` otherwise; therefore; the method returns `false`; as no element meets the criterion of the given expression.

This problem demonstrates the behaviors of the `any?` method. The method will iterate over the collection and evaluate the each element against the given criterion; however; it will not return the same object type of the caller; it will return a boolean; `true` or `false`.





