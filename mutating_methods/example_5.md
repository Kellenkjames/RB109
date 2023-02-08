**What does the following code return? What does it output? Why? What concept does it demonstrate?**

```ruby
def fix(value)
  value[1] = 'x'
  value
end

s = 'abc'
t = fix(s)

# What values do `s` and `t` have? Why?
```
# Written Response:

The local variable `s` is initialized and assigned to the String literal `'abc'` on line 9. The local variable `t` is initialized and assigned to calling the `fix` method invocation with passing the reference `s` as an argument on line 9.

Within the `fix` method definition; the local variable `value`; which is bound to the String `'abc'`; uses the `string[index]` method to assign the second index of `value` to the String literal `x`; this returns the String literal `'axc'`. `value` is referenced on line 6 which returns the String literal `'axc'`; this is the return value of the `fix` method invocation.

`s` returns the String literal `'axc'`; since `s` was mutated using the `string[index]` method within the `fix` method definition; this affects the original object outside of the method.

`t` returns the String literal `'axc'`; the return value of the `fix` method invocation.

This problem demonstrates mutating methods and mutable objects. Strings are mutable objects. String index assignment is a mutating method and will affect the original object outside of the method definition.