**What does the following code return? What does it output? Why? What concept does it demonstrate?**

```ruby
num = 3
num = 2 * num
```
# Written Response:

The local variable `num` is initialized and assigned to the Integer literal `3` on line 4.
`num` is reassigned to the Integer literal `2` times `num`; therefore; `num` returns the Integer literal `6` on line 5.

This problem demonstrates immutable objects and reassignment. Integers are immutable objects. Integers can never be mutated; at best; they can be reassigned or bind to a different variable. In this example; reassignment is used to bind the variable `num` to a new object; the Integer literal `6`; while the original object `3` is left unchanged.


