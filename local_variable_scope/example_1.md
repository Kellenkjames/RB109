**What does the following code return? What does it output? Why? What concept does demonstrate?**

```ruby
a = “Hello”
b = a
a = “Goodbye”

puts a
puts b
```
# Written Response:

The local variable `a` is initialized and assigned to the String `"Hello"` on line 4. The local variable `b` is initialized and assigned to `a` on line 5. `a` is reassigned to the String `"Goodbye"` on line 6.

The `puts` method invocation passes in the reference of `a` as an argument on line 8. Since `a` is now assigned to the String `"Goodbye"`, this is what is output; the method returns `nil`. 
The `puts` method invocation passes in the reference of `b` as an argument on line 9. Since `b` is assigned to `a` and `a` is assigned to the String `"Hello"`; `b` outputs the String `"Hello"`; the method returns `nil`.

This example demonstrates reassignment in Ruby; specifically the fact that reassignment to a variable doesn't mutate the object referenced by that variable; instead; the variable is bound to a different object.