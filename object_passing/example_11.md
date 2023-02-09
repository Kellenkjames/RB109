**What is `arr`? Why? What concept does it demonstrate?**

```ruby
a = [1, 3]
b = [2]
arr = [a, b]
a[1] = 5
arr

# What is `arr`? Why? What concept does it demonstrate?
```
# Written Response:

The local variable `a` is initialized and assigned to the Array `[1, 3]` on line 4. 
The local variable `b` is initialized and assigned to the Array `[2]` on line 5. 
The local variable `arr` is initialized and assigned to the Array `[a, b]` on line 6.

The second index of `a` is reassigned to the Integer `5` on line 7.

Since the second index of `a` is reassigned to the Integer `5` and `arr` points to `a`; `arr` is affected by the index reassignment; therefore; `arr` returns the Array 
`[[1, 5], 2]` on line 8.

This problem demonstrates mutating methods and variables as pointers. Arrays are mutable objects. Unlike Strings using reassignment; reassignment with Arrays mutates the calling object as well as any variables pointing to the object.

