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

The local variable `name` is initialized and assigned to the variable `"jim"`. The `cap` method is called on line 11 and the variable `name` is passed to it as an argument. Within the method definition, the `capitalize!` method is called on `str`; which is bound to the String `"jim"`. Since this is the only expression in the method; the method returns `"Jim"`.

The `puts` method is called on line 12 with the variable `name` passed to it as an argument; since `name` was mutated with the `capitalize!` method within the method definition; it affected the object outside of the method; therefore; the output is `"Jim!"` and the method returns `nil`.

This problem demonstrates object passing and mutable objects. Strings are mutable objects. When a String is passed into a method as an argument and mutated within the method; the original object outside of the method will be affected.

