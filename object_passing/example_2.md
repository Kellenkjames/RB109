**What does the following code return? What does it output? Why? What concept does it demonstrate?**

```ruby
a = "hi there"
b = a
a << ", Bob"

# What are a and b?
```
# Written Response:

The local variable `a` is initialized and assigned to the String `"hi there"` on line 4.
The local variable `b` is initialized and assigned to `a` on line 5. `a` appends the String `", Bob"` on line 6.

Since `a` was mutated; the original object is changed to the String `"hi there, Bob"`; therefore; this is the value that `a` references.
Since `b` is assigned to the reference of `a` and `a` was mutated; `b` is mutated and will return the same String as `a`; `"hi there, Bob"`.

This problem demonstrates mutable objects and variables as pointers. Strings are mutable objects. When an object is mutated; any variable referencing the object that was mutated will be modified as well. Instead of the variable breaking the connection to the object; the object is modified in place.

