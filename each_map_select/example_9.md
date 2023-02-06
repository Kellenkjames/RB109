**What does the following code return? What does it output? Why? What concept does it demonstrate?**

```ruby
arr = [1, 2, 3, 4, 5, 6, 7, 8, 9, 10]

new_array = arr.map do |n|
  n > 1
  puts n
end

p new_array
```
# Written Response:

The local variable `arr` is initialized and assigned to the Array `[1, 2, 3, 4, 5, 6, 7, 8, 9, 10]` to line 4. The local variable `new_array` is initialized and assigned to calling the `map` method on `arr`. The `do...end` alongside the `map` method defines a block on lines 6-9; while the parameter `n` represents each element of `arr`.

Within the block; the expression `n > 1` is evaluated for each `n`; since this expression checks for truthiness; the return value will be a new Array; `[false, true, true, true, true, true, true, true, true, true]`. The `puts` method is called with `n` passed to it as an argument; this outputs each each element of `arr` on a newline; `1 2 3 4 5 6 7 8 9 10` and returns the following array; `[nil, nil, nil, nil, nil, nil, nil, nil, nil, nil]`.

The `p` method is called with `new_array` is passed to it as an argument; this outputs the following; `[nil, nil, nil, nil, nil, nil, nil, nil, nil, nil]` and returns the same object.

This problem demonstrates the behaviors of the `map` method; specifically; the behavior of having a `puts` method as the last line in the method. When `puts` is the last line within a `map` method; the method will return `nil` for each element represented by the block parameter.

