**What does the following code return? What does it output? Why? What concept does it demonstrate?**

```ruby
arr = [1, 2, 3, 4, 5, 6, 7, 8, 9, 10]

new_array = arr.select do |n|
  n + 1
end

p new_array
```
# Written Response:

The local variable `arr` is initialized and assigned to the Array `[1, 2, 3, 4, 5, 6, 7, 8, 9, 10]`. The local variable `new_arr` is initialized and assigned to the `select` method invocation on `arr`.

The `do...end` alongside the `select` method invocation on lines 6-8 defines a block; Within the block; the parameter `n` represents the current element of `arr`. The expression `n + 1` will be evaluated for each `n` in `arr`. Since the expression `n + 1` evaluates as truthy for each `n` in `arr`; this returns the calling object; `[1, 2, 3, 4, 5, 6, 7, 8, 9, 10]`.

The `p` method invocation passes `new_array` in as an argument on line 10; this outputs the original object `[1, 2, 3, 4, 5, 6, 7, 8, 9, 10]` and returns the same object.

This problem demonstrates behaviors of the `select` method. The `select` method always evaluates a given block based on truthiness. In this case, the expression `n + 1` evaluates as truthy for each element in the Array; therefore; the original object is returned. In Ruby, everything is considered truthy with the exception of `false` and `nil`.

