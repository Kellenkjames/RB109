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

The local variable `y` is initialized and assigned to the String `'a'` on line 8. The `increment` method invocation passes in the reference of `y` in as an argument on line 9.

Within the `increment` method definition; the local variable `x` references the String `'a'` and appends the String `'b'`; this returns the String `'ab'` and is the return value of the `increment` method invocation.

Since `y` was mutated from within the `increment` method definition; it changed the original object outside of the method; therefore; the return value is the String `'ab'`.
The `puts` method invocation passes in the reference of `y` as an argument; this outputs the String `'ab'` and the method returns `nil`.

This problem demonstrates object passing. In this example, we can say that Ruby acts as "pass by reference." The original object was passed into the method as an argument and mutated within the method; this changed the original object outside of the method.

