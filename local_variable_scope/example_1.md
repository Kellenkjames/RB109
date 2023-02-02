**What does the following code return? What does it output? Why? What concept does demonstrate?**

```ruby
a = “Hello”
b = a
a = “Goodbye”

puts a
puts b
```

# Written Response:

On line 8, the `puts` method is called and`a` is passed in as an argument. Since `a` is reassigned to the string `"Goodbye"` on line 6, this is the output. The method returns `nil`. On line 9, the `puts` method is called and `b` is passed in as an argument. Since `b` was initialized and assigned to `a` before `a` was reassigned to the string `"Goodbye"`; the string `"Hello"` is the output. The method returns `nil`. This problem demonstrates concepts of reassignment and variables as pointers. Variables do not hold information and are not bound to objects; they act as labels or references for where objects are stored in memory.

