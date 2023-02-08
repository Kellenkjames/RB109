**What does the following code return? What does it output? Why? What concept does it demonstrate?**

```ruby
def fix(value)
  value.upcase!
  value.concat('!')
  value
end

s = 'hello'
t = fix(s)

# What values do `s` and `t` have? Why?
```
# Written Response:

The local variable `s` is initialized and assigned to the String literal `'hello'` on line 10. The local variable `t` is initialized and assigned to the `fix` method invocation with passing the reference `s` as an argument on line 11.

Within the `fix` method definition; the local variable `value` which is bound to the String literal `'hello'`; invokes the `upcase!` method on line 5; this returns the String literal `'HELLO'`.

`value` invokes the `concat` method and passes the reference `('!')` as an argument; the return value is the Sting literal `'HELLO!'` on line 6. `value` is referenced on line 7 which returns the String literal `'HELLO!'`;this is the return value of the method.

`s` returns the String literal `'HELLO!'`; since the original String object was mutated from within the `fix` method definition; it was affected outside of the method definition.
`t` returns the String literal `'HELLO!'`; this is the return value of the `fix` method definition.

This problem demonstrates mutating methods and mutable objects. Strings are mutable objects. When mutable objects are passed into methods and mutated; it will affect the original object from outside of the method.

