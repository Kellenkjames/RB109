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

The method definition `plus` accepts parameters `x` and `y` on line 4.

The local variable `a` is initialized and assigned to the Integer `3` on line 8. The local variable `b` is initialized and assigned to the `plus` method invocation with passing `a` in as the first argument and the Integer `2` as the second argument.

Within the `plus` method definition; the local variable `x` references `a` on line 8 and the local variable `y` references the Integer literal `2` on line 9.
`x` is reassigned to `x + y`; this expression returns the Integer `5` on line 5.

Since `a` was reassigned from within the `plus` method definition; the original object was unchanged; therefore; the return value is the Integer `3`.
`b` returns the Integer `5`; the return value from the `plus` method invocation.

The `puts` method invocation passes `a` in as an argument on line 11. The output is the Integer `3` and the method returns `nil`.
The `puts` method invocation passes `b` in as an argument on line 12. The output is the Integer `5` and the method returns `nil`.

This problem demonstrates object passing and immutable objects. Integers are immutable objects. When passing immutable objects into methods as arguments; we cannot mutate the objects inside the method; they can only be reassigned. Anytime a object is reassigned; the original object is disconnected from the variable. In this example, we could say that Ruby acts like "pass-by-value".



