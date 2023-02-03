**What does the following code return? What does it output? Why? What concept does it demonstrate?**

```ruby
def change_name(name)
  name = 'bob'
end

name = 'jim'
change_name(name)
puts name

# does this reassignment change the object outside the method?
```
# Written Response:

The local variable `name` is initialized and assigned to the String `jim` on line 10. The `change_name` method is called on line 11 and the variable `name` is passed to it as an argument. Within the `change_name` method, the local variable `name` which is bound to the String `jim`; is reassigned to the String `bob`; since this is the only expression in the method; this is the return value.

The `puts` method is called on line 12 and the variable `name` is passed to it as an argument; since from within the method there is a reassignment and reassignment is a non-mutating method; the output of `name` will be it's initialized object; `jim` and the return value is `nil`.

This problem demonstrates passing objects and reassignment. Strings are mutable objects but they are not always mutated when passed into a method as an argument. Reassignment is a non-mutating operation even when working with mutable objects like Strings.

