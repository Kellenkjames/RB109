**What does the following code return? What does it output? Why? What concept does it demonstrate?**

```ruby
a = [1, 2, 3, 4]
b = a
c = a.uniq

# What are a, b, and c? What if the last line was `c = a.uniq!`?
```

# Written Response:

On line 4, `a` is initialized and assigned to the array `[1, 2, 3, 4]`; this is the return value. On line 5, `b` is initialized and assigned to `a`; the return value is the same as object as `a`.

On line 6, `c` is initialized and assigned to the method`a.uniq`. This method will invoke the `.uniq` method on the calling object `a` which returns a new array from containing elements that are not duplicates. The return value is `[1, 2, 3, 4]`.

If the last line was `c = a.uniq!`; `a` the calling object; would modify `self` by removing all duplicates. It would not return a new array. The return value would be the same value as before; `[1, 2, 3, 4]`; except the original object would be permanently modified.

This problem demonstrates the concept of mutating and non-mutating methods. Mutating methods modify the original object and non-mutating methods return a new object. Additionally, multiple variables can reference the same object; mutating an object using a given variable name will be reflected in every other variable that is bound to that object.