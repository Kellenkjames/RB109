**What does the following code return? What does it output? Why? What concept does it demonstrate?**

```ruby
def plus(x, y)
  x = x + y
end

a = 3
b = plus(a, 2)

puts a
puts b
```
# Written Response:

The `plus` method definition accepts parameters `x` and `y` on line 4.

The local variable `a` is initialized and assigned to the Integer `3` on line 8. 
The local variable `b` is initialized and assigned to the `plus` method invocation passing in the reference of `a` as the first argument and the Integer `2` in as the second argument.

Within the `plus` method body; the local variable `x` references the Integer `3` and the local variable `y` references the Integer `2`.
`x` is reassigned to the expression `3 + 2`; this expression returns the Integer `5` on line 5.

Since `a` was reassigned from within the `plus` method body; the original object outside of the method was unchanged; therefore; `a` references the original object; the Integer `3`.
`b` references the Integer `5`; the return value of the `plus` method invocation.

The `puts` method invocation passes the reference of `a` in as an argument on line 11. The output is the Integer `3` and the method returns `nil`.
The `puts` method invocation passes the reference of `b` in as an argument on line 12. The output is the Integer `5` and the method returns `nil`.

This problem demonstrates object passing and immutable objects. Integers are immutable objects. When passing immutable objects into methods as arguments; we cannot mutate the objects inside the method; they can only be reassigned. Anytime a object is reassigned; the original object is disconnected from the variable. In this example, we could say that Ruby acts like "pass-by-value".

