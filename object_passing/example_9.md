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

The `change_name` method definition accepts `name` as a parameter on line 4.

The local variable `name` is initialized and assigned to the String `jim` on line 10.
The `change_name` method invocation passes in the reference of `name` as an argument on line 8.

Within the `change_name` method body; the local variable `name` references the String `'jim'`. `name` is reassigned to the String `'bob'` on line 5; this is the return value of the `change_name` method invocation.

Since `name` was reassigned from inside the `change_name` method body; it did not change the original object outside of the method; therefore; `name` references the String `'jim'`.
The `puts` method invocation passes in the reference `name` as an argument; this outputs the String `'jim'` and returns `nil`.

This problem demonstrates object passing and non-mutating methods. An object was passed into the method and reassigned; this has no effect on the original object outside of the method. Reassignment breaks the connection to the original object binds the variable to a new object. In this example, we can say that Ruby acts as "pass by value". 

