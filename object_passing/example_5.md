**What does the following code return? What does it output? Why? What concept does it demonstrate?**

```ruby
a = 5.2
b = 7.3
a = b
b += 1.1

# What is `a` and `b` ? Why?
```
# Written Response:

The local variable `a` is initialized and assigned to the Integer `5.2` on line 4. The local variable `b` is initialized and assigned to the Integer `7.3` on line 5.

`a` is reassigned to `b` on line 6 and `b` is reassigned to `b` + `1.1` on line 7.

`a` is now `b` and `b` is assigned to the Integer `7.3`; therefore; `a` will output `7.3`. 
`b` will output the total of `b` + `1.1`; this translates to `7.3 + 1.1`; which is `8.4`.

This problem demonstrates reassignment and immutable objects. Integers are immutable objects. If you attempt to change an immutable object, you won't succeed -- at best, you can create a new object, and bind a variable to that object with assignment.

