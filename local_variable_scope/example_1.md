**What does the following code return? What does it output? Why? What concept does demonstrate?**

```ruby
a = “Hello”
b = a
a = “Goodbye”

puts a
puts b
```

# Written Response:

The local variable `a` is initialized and assigned to the String `"Hello"` on line 4. The local variable `b` is initialized and assigned to the variable `a` on line 5. The variable `a` is reassigned to the String `"Goodbye"` on line 6.The `puts` method is called on line 8 with the variable `a` passed to it as an argument; since `a` is now assigned to `"Goodbye"`, this is what is output. The `puts` method is called on line 9 with the variable `b` passed to it as an argument; since `b` was assigned to `a` and `a` was assigned to `"Hello"`; this is what is output.

This example demonstrates reassignment in Ruby; specifically the fact that reassignment to a variable doesn't mutate the object referenced by that variable; instead; the variable is bound to a different object.

