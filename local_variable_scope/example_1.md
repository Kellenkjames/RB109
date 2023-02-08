**What does the following code return? What does it output? Why? What concept does demonstrate?**

```ruby
a = “Hello”
b = a
a = “Goodbye”

puts a
puts b
```
# Written Response:

The local variable `a` is initialized and assigned to the String literal `"Hello"` on line 4. The local variable `b` is initialized and assigned to `a` on line 5. `a` is reassigned to the String literal `"Goodbye"` on line 6.

The method invocation of `puts` passes the reference `a` to it as an argument on line 8. Since `a` is now assigned to the String literal `"Goodbye"`, this is what is output; the method returns `nil`.

The method invocation of `puts` passes the reference `b` to it as an argument on line 9. Since `b` is assigned to `a` and `a` was initialized to the String literal `"Hello"`; `b` outputs the String literal `"Hello"`; the method returns `nil`.

This example demonstrates reassignment in Ruby; specifically the fact that reassignment to a variable doesn't mutate the object referenced by that variable; instead; the variable is bound to a different object.

