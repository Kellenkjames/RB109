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

The local variable `name` is initialized and assigned to the String literal `jim` on line 10. The `change_name` method invocation passes the reference `name` as an argument.

Within the `change_name` method definition; the local variable `name` is bound the to the String literal `'jim'`. `name` is reassigned from the String literal `'jim'` to the String literal `'bob'` on line 5; the return value of the `change_name` method invocation is the String literal `'bob'`.

Since `name` was reassigned from inside the method definition; the return value is the original object; the String literal `'jim'`.
The `puts` method invocation passes the reference `name` as an argument; this outputs the String literal `'jim'`; the method returns `nil`.

This problem demonstrates passing objects and reassignment. Strings are mutable objects but they are not always mutated when passed into a method as an argument. Reassignment is a non-mutating operation even when working with mutable objects like Strings. Reassignment from within a method definition will never change the object outside of the method.

