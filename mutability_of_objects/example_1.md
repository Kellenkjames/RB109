**What does the following code return? What does it output? Why? What concept does it demonstrate?**

```ruby
a = "hi there"
b = a
a = "not there"

# What are a and b?
```
# Written Response:

`a` returns `"not there"` and `b` returns `"hi there"`. What this shows is that reassignment to a variable doesn't mutate the object referenced by that variable; instead, the variable is bound to a different object. The original object is merely disconnected from the variable.