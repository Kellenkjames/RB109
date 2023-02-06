**What does the following code return? What does it output? Why? What concept does it demonstrate?**

```ruby
a = %w(a b c)
a[1] = '-'
p a
```
# Written Response:

The local variable `a` is initialized and assigned to the Array `[a, b, c]` on line 4. The second index of `a` is reassigned to the String `'-'` on line 5.

The `p` method is called while passing `a` to it as an argument. The output and return value is the same; `[a, '-', c]`.

This problem demonstrates mutating methods and mutable objects. Arrays are mutable objects. When using array index reassignment on the original object; it will mutate the object.

