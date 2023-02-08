**What does the following code return? What does it output? Why? What concept does it demonstrate?**

```ruby
def fix(value)
  value << 'xyz'
  value = value.upcase
  value.concat(`!`)
end

s = 'hello'
t = fix(s)

# What values do 's' and 't' have? Why? 
```
# Written Response:

The local variable `s` is initialized and assigned to the String literal `'hello'` on line 10. The local variable `t` is initialized and assigned to the `fix` method invocation with passing the reference `s` as an argument on line 11.

Within the `fix` method definition; the local variable `value` which is bound to the String literal `xyz`; appends the String literal `xyz` on line 5; this returns the String literal `'helloxyz'`.
`value` is reassigned to invoking the `upcase` method on `value` on line 6; this returns the String literal `'HELLOXYZ'`.
The `concat` method is invoked on `value` while passing the reference `('!')` as an argument on line 7; the return value is the String literal `'HELLOXYZ!'`; this is the return value of the `fix` method invocation.

`s` returns the String literal `'helloxyz'`; since `s` was mutated within the `fix` method definition before the reassignment on line 6; it affected the original object outside of the method. The mutated object disconnected from `s` during the reassignment; therefore; any changes that happen at the point of reassignment are ignored by `s`.

`t` returns the String literal `'HELLOXYZ!'`; the return value of the `fix` method invocation.

This problem demonstrates mutating methods before reassignment. Strings are mutable objects. Within a method definition; if a String is mutated *before* its reassigned; the original object will only be affected by mutating methods that occur before the reassignment.

