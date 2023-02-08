**What does the following code return? What does it output? Why? What concept does it demonstrate?**

```ruby
a = 5.2
b = 7.3
a = b
b += 1.1

# What is `a` and `b` ? Why?
```
# Written Response:

The local variable `a` is initialized and assigned to the Integer literal `5.2` on line 4. The local variable `b` is initialized and assigned to the Integer literal `7.3` on line 5.

`a` is reassigned to `b` on line 6.
`b` is reassigned to `b` + `1.1` on line 7.

Since `a` is now `b` and `b` is assigned to the Integer literal `7.3`; `a` returns the Integer literal `7.3`.
Since `b` is now `b` + `1.1`; this translates to `7.3 + 1.1`; therefore; `b` returns the Integer literal `8.4`.

This problem demonstrates reassignment and immutable objects. Integer literals are immutable objects. If you attempt to change an immutable object, you won't succeed -- at best, you can create a new object, and bind a variable to that object with assignment. In this example, one of the variables is reassigned and creates a new reference to the Integer literal object.



