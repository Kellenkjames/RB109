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

The `cap` method definition accepts `str` as a parameter on line 4.

The local variable `name` is initialized and assigned to the String `"jim"` on line 8.
The `cap` method invocation passes in the reference of `name` as an argument on line 9.

Within the `cap` method definition; `str` references the String `"jim"`; the `capitalize!` method invocation is called on `str`; this returns the String `"Jim"`; the `cap` method invocation returns the same value.

Since `name` was mutated from within the `cap` method definition; the object outside of the method is affected; therefore; the return value is the String `"Jim"`.
The `puts` method invocation passes the reference `name` in as an argument on line 10; this outputs the String `"Jim"` and returns `nil`.

This problem demonstrates object passing. When a mutable object is passed into a method as an argument and mutated within the method definition; it will change the original object outside of the method. In this example, we can say that Ruby acts like "pass by reference".

