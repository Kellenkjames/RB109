**What does the following code return? What does it output? Why? What concept does it demonstrate?**

```ruby
a = [1, 2, 3, 4]
b = a
c = a.uniq

# What are a, b, and c? What if the last line was `c = a.uniq!`?
```
# Written Response:

The local variable `a` is initialized and assigned to the Array literal `[1, 2, 3, 4]` on line 4. The local variable `b` is initialized and assigned to `a` on line 5. The local variable `c` is initialized and assigned to `a` invoking the `uniq` method.

Since `a` is assigned to the Array literal `[1, 2, 3, 4]`; this is the return value.
Since `b` is assigned to `a`; the return value is the same as `a`; the Array literal `[1, 2, 3, 4]`.

`c` will return a *new* Array literal containing elements from the original object; `[1, 2, 3, 4]`; that are not duplicates. In this case, it will return a new array with the *same* elements as the original object since there are no duplicates. If the last line was `c = a.uniq!`; it would mutate the original object in place instead of returning a new array.

This problem demonstrates variables as pointers. When calling a non-mutating method on an object; any variable referencing this object will not be changed. Non-mutating methods return new objects and do not modify the original objects.
