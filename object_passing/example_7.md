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

The local variable `a` is initialized and assigned to the Integer `3` on line 8. The local variable `b` is initialized and assigned to the following; calling the `plus` method and passing in `a` as the first argument and the Integer `2` as the second argument.

On line 5, the local variable `x` is reassigned to `x + y`; since `x` is bound to the Integer `2` and `y` is bound to the Integer `3`; the return value of the method is `3 + 2`; which is the Integer `5`.

The `puts` method is called on line 11 and the variable `a` is passed to it as an argument; since `a` was initialized to the Integer `3`; this is what is output and the method returns `nil`.

The `puts` method is called on line 12 and the variable `b` is passed to it as an argument; since `b` is assigned to the method invocation of `plus` with `a` passed to it as the first argument, and the Integer `2` passed to it as the second argument; the output is the Integer `5` and the method returns `nil`.

This problem demonstrates object passing and immutable objects. Integers are immutable objects. When passing immutable objects into methods as arguments; we cannot mutate the objects inside the method; they can only be reassigned.

