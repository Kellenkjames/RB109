**What does the following code return? What does it output? Why? What concept does it demonstrate?**

```ruby
arr = [1, 2, 3, 4, 5, 6, 7, 8, 9, 10]

arr.each { |n| puts n }
```
# Written Response:

The local variable `arr` is initialized and assigned to the Array `[1, 2, 3, 4, 5, 6, 7, 8, 9, 10]` on line 4. The `{}` alongside the `each` method defines a block on line 6. The block is passed to the `each` method as as argument; within the block; `n` is the parameter that represents each element of `arr`. 

The `puts` method is called with `n` passed to it as an argument; this will output each Integer of `arr` onto a newline; `1 2 3 4 5 6 7 8 9 10`; The method returns the original object `[1, 2, 3, 4, 5, 6, 7, 8, 9, 10]`. 

This problem demonstrates the behaviors of the `each` method. The `each` method iterates over array elements and returns `self`. In this example, each array element is printed to a newline before the calling object is returned.


