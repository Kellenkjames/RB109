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

The local variable `name` is initialized and assigned to the String literal `"jim"` on line 8. The `cap` method invocation passes the reference `name` to it as an argument on line 9.

Within the `cap` method definition; `str` invokes the `capitalize!` method. Since `str` represents a local variable and is bound to the String literal `"jim'`; the method returns the String literal `"Jim"`; the `cap` method definition returns the same value.

Since `name` was mutated from within the `cap` method definition; the object outside of the method is affected; therefore; the return value is the String literal `"Jim"`.

The `puts` method invocation passes the reference `name` as an argument on line 10; this outputs the String literal `"Jim"` and returns `nil`.

This problem demonstrates object passing and mutable objects. Strings are mutable objects. When a String is passed into a method as an argument and mutated within the method; the original object outside of the method will be affected.

