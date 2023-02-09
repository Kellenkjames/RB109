**What does the following code return? What does it output? Why? What concept does it demonstrate?**

```ruby
a = "hi there"
b = a
a = "not there"

# What are a and b?
```
# Written Response:

The local variable `a` is initialized and assigned to the String `"hi there"` on line 4.
The local variable `b` is initialized and assigned to `a` on line 5. 
`a` is reassigned to the String `"not there"` on line 6.

Since `a` is now assigned to the String `"not there"`; this is what is output.
Since `b` is assigned to `a` before `a` is reassigned; it will output the String `"hi there"`.

This problem demonstrates reassignment in Ruby; reassignment doesn't mutate the object referenced by that variable, instead, the variable is bound to a different object. The original object is merely disconnected from the variable.

