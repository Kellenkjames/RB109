**What does the following code return? What does it output? Why? What concept does it demonstrate?**

```ruby
array = [1, 2, 3, 4, 5]

array.select do |num|
  puts num if num.odd?
end
```
# Written Response:

The local variable `array` is initialized and assigned to the Array `[1, 2, 3, 4, 5]` on line 4. The `do..end` alongside the `select` method invocation defines a block on lines 6-8. Within the block, the parameter `num` represents the current element of `array` and the block is called on each `num`.

The `puts` method invocation passes `num` in as an argument and checks if `num` is an odd number for each `num`; this will print out every odd number in the Array `[1, 3, 5]` on a newline and return an empty Array `[]`.

This problem demonstrates behaviors of the `select` method. The `select` method calls the block on each element of the Array and returns a new Array with elements that evaluate as truthy. In this example, the `puts` method invocation is the last line of the block and returns `nil`, which means; the block will always evaluate to false and the Array selects nothing.

