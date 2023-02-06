**What does the following code return? What does it output? Why? What concept does it demonstrate?**

```ruby
arr = [1, 2, 3, 4, 5, 6, 7, 8, 9, 10]

new_array = arr.select do |n| 
  n + 1
  puts n
end

new_array
```
# Written Response:

The local variable `arr` is initialized and assigned to the Array `[1, 2, 3, 4, 5, 6, 7, 8, 9, 10]` on line 4. The local variable `new_arr` is initialized and assigned to calling the `select` method on `arr` while passing the `do...end` to it as an argument on; line 6.

The `do...end` alongside the `select` method defines a block on lines 6-9; within the block; the expression `n + 1` is evaluated on line 7; while `n`; the block parameter; represents the current element of `arr`. The expression on line 7 is ignored since the `select` method only considers truthiness.

The `puts` method is called on line 8 where `n` is passed to it as an argument; since the `puts` method always returns `nil`; the output is an empty array `[]`. `new_array` returns an empty array `[]` on line 11.

This problem demonstrates the behaviors of the `select` method. The `select` method only considers truthiness; therefore, math expressions within the block are ignored. In addition, Ruby methods always evaluates the expression of the last line unless there is an explicit return that comes before it. The `puts` method is called on the last line of the `select` method; it will always return `nil`; same as an empty array `[]`.

