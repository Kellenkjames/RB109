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

The local variable `name` is initialized and assigned to the String `jim` on line 10. The method definition `change_name` is called with the reference `name` passed to it as an argument. 
Within the method definition `change_name`; the local variable `name` is bound the to the String `'jim'`. `name` is reassigned from the String `'jim'` to the String `'bob'` on line 5.

Since `name` was reassigned from inside the method definition; the return value is the original object; the String `'jim'`.
The method call `change_name(name)` returns the String `'bob'`.
The `puts` method is called with the reference `name` being passed to it as an argument; this outputs the String `'jim'`. The method returns `nil`.

This problem demonstrates passing objects and reassignment. Strings are mutable objects but they are not always mutated when passed into a method as an argument. Reassignment is a non-mutating operation even when working with mutable objects like Strings. Reassignment from within a method definition will never change the object outside of the method.

