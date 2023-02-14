**What does the following code return? What does it output? Why? What concept does it demonstrate?**

```ruby
arr = [1, 2, 3, 4, 5, 6, 7, 8, 9, 10]

arr.each { |n| puts n }
```
# Written Response:

The local variable `arr` is initialized and assigned to the Array `[1, 2, 3, 4, 5, 6, 7, 8, 9, 10]` on line 4. The `each` method is invoked on the reference of `arr` on line 6.

The `{}` alongside the `each` method invocation defines a block on line 6. The block parameter `n` represents the current element of `arr`.

The `puts` method invocation passes in the reference of `n` as an argument; this will output each `n` in `arr` onto a newline; `1 2 3 4 5 6 7 8 9 10` and the method returns the same object.

This problem demonstrates the behaviors of the `each` method. The `each` method iterates over array elements and returns `self`. In this example, each array element is printed to a newline before the calling object is returned.


