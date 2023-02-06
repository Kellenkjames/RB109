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

The local variable `names` is initialized and assigned to the Array `['bob', 'kim']` on line 8. The `add_name` method is called with `names` passed to it as the first argument and the String `'jim'` passed to it as the second argument; on line 9.

Within the method definition; the local variable `arr` is bound to the Array `['bob', 'kim']` and is reassigned to the expression `arr << name` on line 5; The local variable `name` is bound to the String `'jim'`; therefore; the expression `arr << name` returns the Array `['bob', 'kim', 'jim']`; this is also the return value of the method.

`names` returns the Array `['bob', 'kim', 'jim]`; since the original object was mutated within the method definition; it affects the original object outside of the method definition.

`add_name(names, 'jim')` returns the same Array as `names`; `['bob', 'kim', 'jim']`. The `puts` method is called on line 11 with `names` passed to it as an argument. The output are the Strings `'bob', 'kim', 'jim'` each printed on a newline and the method returns `nil`.

This problem demonstrates mutating methods and mutable objects. Arrays are mutable objects. When an Array object is passed to a method as an argument and mutated from within the method definition; the original object outside of the method will be affected.


