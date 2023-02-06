**What does the following code return? What does it output? Why? What concept does it demonstrate?**

```ruby
num = 3
num = 2 * num
```
# Written Response:

The local variable `num` is initialized and assigned to the Integer `3` on line 5. `num` is reassigned to the expression `2 * num` on line 6; therefore; `num` returns the Integer 6. 

This problem demonstrates immutable objects and reassignment. Integers are immutable objects. Integers can never be mutated; at best; they can be reassigned or bind to a different variable. In this example; reassignment is used to bind the variable `num` to a new object; the Integer `6`; while the original object `3` is left unchanged.


