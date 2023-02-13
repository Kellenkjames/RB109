**What does the following code return? What does it output? Why? What concept does it demonstrate?**

```ruby
a = %w(a b c)
a[1] = '-'
p a
```
# Written Response:

The local variable `a` is initialized and assigned to the Array `['a', 'b', 'c']` on line 4.
`a` invokes an Array element setter method that assigns the second index of `a` to the String `'-'` on line 5.
The `p` method invocation passes in the reference of `a` in as an argument; this outputs and returns the Array `['a', '-', 'c']` on line 6.

This problem demonstrates mutating methods. The Array setter method is a mutating method that will affect the original object that it was called on.