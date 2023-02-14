**What does the following code return? What does it output? Why? What concept does it demonstrate?**

```ruby
{ a: "ant", b: "bear", c: "cat" }.any? do |key, value|
  value.size > 4
end
```
# Written Response:

The `any` method invocation is called on the Hash literal `{ a: "ant", b: "bear", c: "cat" }` on line 4.

The `do...end` alongside the `any?` method invocation defines a block on lines 4-6. The block parameters `key` and `value` represent the current key-value pair of the Hash `{ a: "ant", b: "bear", c: "cat" }`.

Within the block; the expression `value.size > 4` is called on each `key` and `value` pair within the Hash literal `{ a: "ant", b: "bear", c: "cat" }`. The `any?` method returns the boolean `true` if any element satisfies the given expression; `false` otherwise; therefore; the method returns boolean `false`; as no `value` meets the criteria of the given expression.

This problem demonstrates the behaviors of the `any?` method. The method will iterate over the collection and evaluate each element against the given criteria; however; it will not return the same object type of the calling object; it will return a boolean; `true` or `false`.


