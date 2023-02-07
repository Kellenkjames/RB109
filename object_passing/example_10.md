**What does the following code return? What does it output? Why? What concept does it demonstrate?**

```ruby
def cap(str)
  str.capitalize!
end

name = "jim"
cap(name)
puts name

# does this affect the object outside the method?
```

# Written Response:

The local variable `name` is initialized and assigned to the String `"jim"` on line 8. The `cap` method invocation passes the reference `name` to it as an argument.  

This problem demonstrates object passing and mutable objects. Strings are mutable objects. When a String is passed into a method as an argument and mutated within the method; the original object outside of the method will be affected.

