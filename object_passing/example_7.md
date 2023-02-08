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

The local variable `a` is initialized and assigned to the Integer literal `3` on line 8. The local variable `b` is initialized and assigned to the `plus` method invocation with passing the value `a` as the first argument and the Integer literal `2` as the second argument.

Within the `plus` method definition; the local variable `x` is bound to the Integer literal `3` and the local variable `y` is bound to the Integer literal `2`.
`x` is reassigned to `x + y`; this expression returns the Integer literal `5` on line 5.

Since `a` was reassigned from within the `plus` method definition; it returns its original object; the Integer literal `3`.
`b` returns the Integer literal `5`.

The `puts` method invocation passes the value `a` as an argument on line 11. The output is the Integer literal `3` and the method returns `nil`.
The `puts` method invocation passes the value `b` as an argument on line 12. The output is the Integer literal `5` and The method returns `nil`.

This problem demonstrates object passing and immutable objects. Integer literals are immutable objects. When passing immutable objects into methods as arguments; we cannot mutate the objects inside the method; they can only be reassigned. Anytime a object is reassigned; the original object is disconnected from the variable.