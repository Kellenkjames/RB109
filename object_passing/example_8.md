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

The local variable `y` is initialized and assigned to the String `a` on line 8. The `increment` method is called on line 9 with `y` passed to it as an argument.

The local variable `x`; which is bound to the String `'a'` appends the String `'b'` on line 5; since this is the only expression in the method; the method implicitly returns the String `'ab'`.

The `puts` method is called on line 10 and the variable `y` is passed to it as an argument; since `y` was passed into the `increment` method as an argument and the argument was mutated inside the method; the output is the String `'ab'` and the method returns `nil`.

This problem demonstrates object passing and mutable objects. Strings are mutable objects. When a String object is passed into a method as an argument and the object is mutated inside the method; it will mutate the original object outside of the method.


