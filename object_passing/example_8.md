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

The local variable `y` is initialized and assigned to the String `'a'` on line 8. The `increment` method invocation passes the reference `y` as an argument on line 9.

Within the `increment` method definition; the local variable `x`; which is bound to the String literal `'a'`; appends the String literal `'b'` on line 5; this returns the String literal `'ab'`; the String literal `'ab'` is the return value of the `increment` method invocation.

Since `y` was mutated from within the `increment` method definition; the return value is the String literal `'ab'`.

The `puts` method invocation passes the reference `y` as an argument; this outputs the String literal `'ab'` and the method returns `nil`.

This problem demonstrates object passing and mutable objects. Strings are mutable objects. When a reference is passed into a method as an argument and the object is mutated inside the method; it will mutate the original object outside of the method.

