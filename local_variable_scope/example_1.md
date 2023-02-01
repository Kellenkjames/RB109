**What does the following code return? What does it output? Why? What concept does demonstrate?**

```ruby
a = “Hello”
b = a
a = “Goodbye”

puts a
puts b
```

# Written Response:

On line 4, the local variable `a` is initialized and assigned to the string `"Hello"`.
On line 5, the local variable `b` is initialized and assigned to `a`.
On line 6, `a` is re-assigned to the string `"Goodbye"`.

On line 8, we invoke the `puts` method and pass in `a` as an argument. Since we re-assigned `a` to the string `"Goodbye"` on line 6, this is the output. The method returns `nil`.

On line 9, we invoke the `puts` method and pass in `b` as an argument. Since `b` was initialized and assigned to `a` before `a` was re-assigned to the string `"Goodbye"`; the string `"Hello"` is the output. The method returns `nil`.

This problem demonstrates concepts of re-assignment and variables as pointers. Variables do not hold information and are not bound to objects; they act as labels or references for where objects are stored in memory. This explains how variables can point to objects that are different from their initialized values through re-assignment.


