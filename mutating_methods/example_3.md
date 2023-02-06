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

The local variable `s` is initialized and assigned to the String `'hello'` on line 10. The local variable `t` is initialized and assigned to calling the `fix` method while passing in `s` as an argument; on line 11.

Within the method definition; the local variable `value` which is bound to the String `xyz`; appends the String `xyz` to itself; on line 5. `value` is reassigned on line 6 while calling the `upcase` method on itself. On line 7, the `concat` method is called on `value` while passing `('!')` to it as an argument. The return value of the method is the String `'HELLOXYZ!'`.

The variable `s` returns the String `'helloxyz'`; since the argument `s` was mutated inside the method definition on line 5 and before the reassignment on line 6; it affected the original object outside of the method.

The variable `t` returns the String `'HELLOXYZ!'`; since the variable `value` was reassigned on line 6; the method returns a new String and doesn't affect the original object outside of the method definition.

This problem demonstrates mutating methods before reassignment. Strings are mutable objects. Within a method definition; if a String is mutated *before* its reassigned; the original object will only be affected by mutating methods that occur before the reassignment.

