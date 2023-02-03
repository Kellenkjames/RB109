**What does the following code return? What does it output? Why? What concept does it demonstrate?**

```ruby
a = "hi there"
b = a
a = "not there"

# What are a and b?
```
# Written Response:

The local variable `a` is initialized and assigned to the String `"hi there"` on line 4. The local variable `b` is initialized and assigned to `a` on line 5. `a` is reassigned to the String `"not there"`.

Since `a` is now the String `"not there"`; this is what is output. `b` is assigned to `a` before `a` is reassigned; therefore, it will output the String `"hi there"`.

This problem demonstrates reassignment in Ruby; reassignment is a non-mutating operation. When two variables are pointing to the same object and one of the variables is reassigned; the variable that is reassigned breaks the binding of the reference to the original object.

