**What does the following code return? What does it output? Why? What concept does it demonstrate?**

```ruby
{ a: "ant", b: "bear", c: "cat" }.any? do |key, value|
  value.size > 4
end
```
# Written Response:

The `any` method invocation is called on the Hash literal `{ a: "ant", b: "bear", c: "cat" }` on line 4.

The `do...end` alongside the `any?` method invocation defines a block on lines 4-6. The block parameters `key` and `value` represent the current key-value pairs of the Hash literal `{ a: "ant", b: "bear", c: "cat" }`.

Within the block; the expression `value.size > 4` is called on each `value` within the Hash literal `{ a: "ant", b: "bear", c: "cat" }`. The `any?` method returns the boolean `true` if any `value` evaluates as true based on the given expression; `false` otherwise; The method returns the boolean `false`; as no `value` evaluates as true based on the given expression.

This problem demonstrates the behaviors of the `any?` method. The method will iterate over the collection call the block on each element in the collection. If any element in the collection evaluates as true; the method will return the boolean `true`; `false` otherwise.


