**What does the following code return? What does it output? Why? What concept does it demonstrate?**

```ruby
def add_name(arr, name)
  arr = arr + [name] # returns a new Array
  name
end

names = ['bob', 'kim']
add_name(names, 'jim')
puts names
```
# Written Response:

The local variable `names` is initialized and assigned to the Array `['bob', 'kim']` on line 9. The `add_name` method is called on line 10 while passing in `names` as the first argument and the String `jim` as the second argument.

Within the method definition; the local variable `arr`; which is bound to the Array `['bob', 'kim']`; is reassigned to the expression `arr + [name]` on line 5. The local variable `name` is bound to the String `'jim'`; therefore; line 5 returns a new Array; `['bob', 'kim', 'jim']`. The local variable `name` is returned on line 6; the return value is the String `'jim'`; which is the return value of the method.

`names` will return the original Array object; `['bob', 'kim']`; since `names` was not mutated inside the method definition; the original object was left unchanged.

`add_name(names, 'jim')` will return `['bob', 'kim', 'jim']` on line 10. The `puts` method is called on line 11 with `name` passed to it as an argument. The output will be the Strings `'bob'` and `'kim'` each on a newline and the return value is `nil`.

This problem demonstrates reassignment and mutable objects. Arrays are mutable objects. Within the method definition, the original object is reassigned with the `#+`; returns a new array and left the original object outside of the method unchanged.






