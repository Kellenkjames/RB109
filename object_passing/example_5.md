**What does the following code return? What does it output? Why? What concept does it demonstrate?**

```ruby
a = 5.2
b = 7.3
a = b
b += 1.1

# What is `a` and `b` ? Why?
```
# Written Response:

The local variable `a` is initialized and assigned to the Integer `5.2` on line 4.
The local variable `b` is initialized and assigned to the Integer `7.3` on line 5.

`a` is reassigned to `b` on line 6.
`b` is reassigned to the Integer `7.3` plus the Integer `1.1` which equals the Integer `8.4`.

Since `a` is reassigned to the reference of `b` and `b` is assigned to the Integer `7.3`; `a` references the Integer `7.3`.
Since `b` is reassigned to the Integer `8.4`; `b` references the Integer `8.4`.

This problem demonstrates reassignment and immutable objects. Integers are immutable objects. If you attempt to change an immutable object, you won't succeed -- at best, you can create a new object, and bind a variable that object with assignment. In this example, one of the variables is reassigned which creates a new reference to the Integer object.

