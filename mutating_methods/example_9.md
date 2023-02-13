**What does the following code return? What does it output? Why? What concept does it demonstrate?**

```ruby
def add_name(arr, name)
  arr = arr + [name]
  name
end

names = ['bob', 'kim']
add_name(names, 'jim')
puts names
```
# Written Response:

The method definition `add_name` accepts `arr` and `name` as parameters on line 4.

The local variable `names` is initialized and assigned to the Array `['bob', 'kim']` on line 9. The `add_name` method invocation passes in the reference of `names` in as the first argument and the String literal `jim` as the second argument.

Within the  `add_name` method definition; the local variable `arr`; references the Array `['bob', 'kim']` and the local variable `name` references the String `'jim'`. `arr` is reassigned to add `[name]` to `arr`; this returns the Array `['bob', 'kim', 'jim']` on line 5. `name` is referenced on line 6 which returns the String `'jim'`; this is the return value of the `add_name` method invocation.

`names` now references the Array `['bob', 'kim']`. Since `names` was not mutated within the `add_name` method definition; the original object outside of the method was unchanged.
The `puts` method invocation passes in the reference of `names` in as an argument on line 11; this outputs each String of the Array `['bob', 'kim']` on a newline and returns `nil`.

This problem demonstrates object passing and non-mutating methods. In this example, we can say that Ruby acts as "pass-by-value". When a mutable object is passed into a method invocation as an argument and the method is not mutated inside the method; the original object outside of the method is left unchanged. In addition, the Array `#+` method; which adds two arrays together; returns a new array and doesn't affect the original object.

