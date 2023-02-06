**What does the following code return? What does it output? Why? What concept does it demonstrate?**

```ruby
array = [1, 2, 3, 4, 5]

array.select do |num|
  puts num if num.odd?
end
```
# Written Response:

The local variable `array` is initialized and assigned to the Array `[1, 2, 3, 4, 5]` on line 4. The `do..end` alongside the `select` method defines a block on lines 6-8. The block parameter `num` represents the current element of `array` and the block is passed to the `select` method as an argument.

The `puts` method is called on line 7 and the expression `num if num.odd?` is passed to it as an argument; this outputs the Integers `[1, 3, 5]` each on a newline and the method returns an empty array `[]`.

The `puts` method always returns `nil`; or completely empty; therefore; an empty array `[]` is returned.

This problem demonstrates the behaviors of the `select` method. The `select` method selects all elements of the array which evaluate as truthy and returns a *new* array; it doesn't mutate the original object.

