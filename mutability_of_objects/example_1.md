**What does the following code return? What does it output? Why? What concept does it demonstrate?**

```ruby
a = "hi there"
b = a
c = b
a << ", Bob"

# What are a and b?
```

# Written Response:

`a` and `b` have the same return value; `"hi there, Bob"`. Strings are mutable objects. When we apply the `<<` operator on `a`; it will append the string `", Bob"` to the end of the `"hi there"`; which is the initialized value of `a`. This is a mutating method and modifies the calling object `a` as well as any objects that are referencing `a`; in this case; `b` is the object that is referencing `a`.

This problem demonstrates the concept of mutability of Ruby objects and variable references. Multiple variables can reference the same object; mutating an object using a given variable name will be reflected in every other variable that is bound to that object.
