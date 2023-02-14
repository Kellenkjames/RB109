**What does the following code return? What does it output? Why? What concept does it demonstrate?**

```ruby
def increment(x)
  x << 'b'  
end

y = 'a'
increment(y)
puts y
```
# Written Responses:

The `increment` method definition accepts `x` as a parameter on line 4.

The local variable `y` is initialized and assigned to the String `'a'` on line 8. The `increment` method invocation passes in the reference of `y` as an argument on line 9.

Within the `increment` method body; the local variable `x` references the String `'a'` and appends the String `'b'`; this returns the String `'ab'`.

Since `y` was mutated from within the `increment` method body; it changed the original object outside of the method; therefore; `y` references the String `'ab'`.
The `puts` method invocation passes in the reference of `y` as an argument; this outputs the String `'ab'` and returns `nil`.

This problem demonstrates object passing and mutable objects. Strings are mutable objects. The original object was passed into the method as an argument and mutated within the method; this changed the original object outside of the method. In this example, we can say that Ruby acts like "pass by reference."