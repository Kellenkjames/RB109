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

The method definition `add_names` accepts `arr` and `name` as parameters on line 4.

The local variable `names` is initialized and assigned to the Array `['bob', 'kim']` on line 8. The `add_name` method invocation passes in `names` as the first argument and the String literal `'jim'` as the second argument on line 9.

Within the `add_name` method definition; the local variable `arr` references the Array `['bob', 'kim']` and is reassigned to `arr` appending `name`; The local variable `name` references the String `'jim'`; therefore; the method returns the Array `['bob', 'kim', 'jim']`.

`names` returns the Array `['bob', 'kim', 'jim]`; since the original object was mutated within the `add_name` method definition; it affects the original object outside of the method.
The `puts` method invocation passes `names` in as an argument; this outputs each String in the Array `['bob', 'kim', 'jim']` on a newline and returns `nil`.

This problem demonstrates object passing and mutating methods. In this example, we can say that Ruby acts as "pass by reference". When a mutable object is passed into a method invocation as an argument and mutated within the method; it will affect the original object outside of the method.
