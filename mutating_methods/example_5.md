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

The local variable `s` is initialized and assigned to the String `'abc'` on line 9. The local variable `t` is initialized and assigned to calling the `fix` method while passing `s` to it as an argument; on line 10.

Within the method definition; the local variable `value`; which is bound to the String `'abc'`; reassigns the second index to the String `'x'`. On line 6, `value` is returned; the String `axc'`.

`s` returns the String `axc`; since `s` was mutated using index reassignment within the method definition; this affects the original object outside of the method.

`t` returns the String `axc`; the same as the return value of the method invocation of `fix` with `s` passed to it as an argument.

This problem demonstrates mutating methods and mutable objects. Strings are mutable objects. Index reassignment is a mutating operation and will affect the original object outside of the method definition.