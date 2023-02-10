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

The local variable `arr` is initialized and assigned to the Array `[1, 2, 3, 4, 5, 6, 7, 8, 9, 10]` on line 4. The local variable `new_arr` is initialized and assigned to the `select` method invocation on `arr`.

The `do...end` alongside the `select` method invocation defines a block on lines 6-9; within the block; the parameter `n` represents the current element of `arr`. On each loop iteration, the expression ` n + 1` will be evaluated for each `n` on line 7. Since the expression evaluates as truthy for each `n`; this returns the calling object `[1, 2, 3, 4, 5, 6, 7, 8, 9, 10]`.

The `puts` method invocation passes `n` as an argument on line 8; this outputs each element of the calling object `[1, 2, 3, 4, 5, 6, 7, 8, 9, 10]` on a new line and returns an empty Array `[]`.

`new_array` is referenced on line 11 and returns an empty Array `[]`.

This problem demonstrates behaviors of the `select` method. The `select` method calls the block for each element and returns a new Array with elements that evaluate as truthy. In this example, the `puts` method invocation is the last line of the method and it returns `nil`; which always evaluates to false. In Ruby, everything is truthy with the exception of `false` and `nil`.

