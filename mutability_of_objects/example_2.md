**What does the following code return? What does it output? Why? What concept does it demonstrate?**

```ruby
a = "hi there"
b = a
a << ", Bob"

# What are a and b?
```
# Written Response:

The local variable `a` is initialized and assigned to the String `"hi there"` on line 4. The local variable `b` is initialized and assigned to the variable `a` on line 5. On line 6, the append method is invoked on `a` and the String `", Bob"` is passed to it as an argument.

Since `a` was modified with a mutating method; the original object is changed to `"hi there, Bob"`; therefore; this is what is output. Since `b` was assigned to `a` and `a` was mutated; it will output the same String as `a`; `"hi there, Bob"`.

This problem demonstrates mutable objects In Ruby, Strings are mutable objects. When an object is mutated; any variable referencing the object that was mutated will be modified as well. Instead of the variable breaking the connection to the object; the object is modified in place.