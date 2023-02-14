**What does the following code return? What does it output? Why? What concept does it demonstrate?**

```ruby
a = [1, 2, 3, 4]
b = a
c = a.uniq

# What are a, b, and c? What if the last line was `c = a.uniq!`?
```
# Written Response:

The local variable `a` is initialized and assigned to the Array `[1, 2, 3, 4]` on line 4.
The local variable `b` is initialized and assigned to `a` on line 5.
The local variable `c` is initialized and assigned to calling the `uniq` method invocation on `a`.

Since `a` is not mutated anywhere in the program; it references the original Array `[1, 2, 3, 4]`.
Since `b` is assigned to the reference of `a`; it references the original Array `[1, 2, 3, 4]`.

`c` will return a *new* Array containing elements from the original object; `[1, 2, 3, 4]`; that are not duplicates. In this case, it will return a new array with the *same* elements as the original object. 
If the last line was `c = a.uniq!`; this would mutate the original object in place instead of returning a new array.

This problem demonstrates non-mutating methods. When calling a non-mutating method on an object; any variable referencing this object will not be affected. Non-mutating methods return new objects and do not modify the original objects.

