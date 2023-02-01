**What does the following code return? What does it output? Why? What concept does it demonstrate?**

```ruby
a = 5.2
b = 7.3
a = b
b += 1.1

# What is `a` and `b` ? Why?
```

# Written Response:

`a` returns `7.3` because it was reassigned to `b` on line 6 and `b` is pointing to the integer `7.3`. 

`b` returns `8.4` because it uses the shorthand operator to perform addition; `7.3 + 1.1` which results in `8.4` and is reassigned back to `b`.

This problem demonstrates the concept of immutable objects and reassignment. In Ruby, integers are immutable objects. In this example, we use the shorthand operator to calculate the total of two integers. The shorthand operator is reassignment and doesn't mutate the object. Instead, it binds a different object to the variable.

