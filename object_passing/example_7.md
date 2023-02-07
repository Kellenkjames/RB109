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

The local variable `a` is initialized and assigned to the Integer `3` on line 8. The local variable `b` is initialized and assigned to calling the `plus` method with passing the value `a` to it as the first argument and the Integer `2` as the second argument.

Within the method definition `plus`; the local variable `x` is bound to the Integer `3` and the local variable `y` is bound to the Integer `2`.
`x` is reassigned to `x + y`; this expression returns the Integer `5` on line 5.

Since `a` was reassigned within the method definition `test`; it returns its original object; the Integer `3`.
`b` returns the Integer `5`.

The `puts` method is called with the value `a` passed to it as an argument on line 11. The output is the Integer `3`. The method returns `nil`.
The `puts` method is called with the value `b` passed to it as an argument on line 12. The output is the Integer `5`. The method returns `nil`.

This problem demonstrates object passing and immutable objects. Integers are immutable objects. When passing immutable objects into methods as arguments; we cannot mutate the objects inside the method; they can only be reassigned. Anytime a object is reassigned; the original object is disconnected from the variable.