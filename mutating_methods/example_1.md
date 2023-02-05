**What does the following code return? What does it output? Why? What concept does it demonstrate?**

```ruby
def fix(value)
  value.upcase!
  value.concat('!')
  value
end

s = 'hello'
t = fix(s)
```
# Written Response:

The local variable `s` is initialized and assigned to the String `'hello'` on line 10. The local variable `t` is initialized and assigned to calling the `fix` method while passing in `s` as an argument on line 11.

Within the `fix` method definition; the local variable `value`; which is bound to the String `'hello'` calls the `upcase!` method on line 5; this returns `'HELLO'`.

The local variable `value` calls the `concat` method on line 6 and passes the String `('!')` as an argument; since `value` is now the String `'HELLO!'`; this is the return value of `value` of line 7; the method returns the same value.

The variable `s` returns `'HELLO!'`; since the original String object was mutated from within the method definition; it was affected outside of the method definition. The variable `t` returns `'HELLO!'`; the return value of calling the `fix` method while passing the variable `s` to it as an argument.

This problem demonstrates mutating methods and mutable objects. Strings are mutable objects. When mutable objects are passed into methods and mutated; it will affect the original object from outside of the method.

