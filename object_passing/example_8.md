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

The local variable `y` is initialized and assigned to the String `'a'` on line 8. The method definition `increment` is called with the reference `y` passed to it as an argument on line 9.
The local variable `x` which is bound to the String `a`; appends the String `b` on line 5. This returns the String `'ab'`.

Since `y` was mutated from within the method definition `increment`; the return value is the String `'ab'`.
The method call `increment(y)` returns the String `'ab'`.
The `puts` method is called with the reference `y` passed to it as an argument; this outputs the String `'ab'`. The method returns `nil`.

This problem demonstrates object passing and mutable objects. Strings are mutable objects. When a reference is passed into a method as an argument and the object is mutated inside the method; it will mutate the original object outside of the method.


