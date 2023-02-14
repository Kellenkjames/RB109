**What does the following code return? What does it output? Why? What concept does it demonstrate?**

```ruby
def add_name(arr, name)
  arr = arr << name
end

names = ['bob', 'kim']
add_name(names, 'jim')
puts names
```
# Written Assessment:

The `add_names` method definition accepts `arr` and `name` as parameters on line 4.

The local variable `names` is initialized and assigned to the Array `['bob', 'kim']` on line 8. The `add_name` method invocation passes in the reference of `names` in as the first argument and the String literal `'jim'` as the second argument on line 9.

Within the `add_name` method body; the local variable `arr` references the Array `['bob', 'kim']` and the local variable `name` references the String literal `jim`.
`arr` is reassigned to append the String `'jim'` to `self`; which returns the Array `['bob', 'kim', 'jim']`.

`names` now references the Array `['bob', 'kim', 'jim]`; since the original object was mutated within the `add_name` method body; it affects the original object outside of the method.
The `puts` method invocation passes in the reference of `names` as an argument; this outputs each String in the Array `['bob', 'kim', 'jim']` on a newline and returns `nil`.

This problem demonstrates object passing and mutating methods. When a mutable object is passed into a method invocation as an argument and mutated within the method; it will affect the original object outside of the method. In this example, we can say that Ruby acts like "pass by reference".