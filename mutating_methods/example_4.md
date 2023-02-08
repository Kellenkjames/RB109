**What does the following code return? What does it output? Why? What concept does it demonstrate?**

```ruby
def fix(value)
  value = value.upcase! # reassignment with a mutating method will affect the object outside of the method.
  value.concat('!')
end

s = 'hello'
t = fix(s)

# What values do `s` and `t` have? Why?
```
# Written Response:

The local variable `s` is initialized and assigned to the String literal `'hello'` on line 9. The local variable `t` is initialized and assigned to the `fix` method invocation with passing the reference `s` as an argument on line 10.

Within `fix` the method definition; the local variable `value` which is bound to the String `'hello'`; is reassigned to the `upcase!` method invocation; this returns the String literal `'HELLO'`.
The `concat` method is invoked on `value` while the reference `('!')` is passed as an argument; this returns the String literal `'HELLO!'`.

`s` returns the String literal; `HELLO!`; Since `s` is reassigned and mutated within the `fix` method definition; the object outside of the method is affected.
`t` returns the String literal `'HELLO!'`; the return value of the `fix` method invocation.

This problem demonstrates mutating methods and reassignment. When an object is reassigned with a mutating method invoked on the object; it will affect the object outside of the method. This is an important distinction as normal reassignment will disconnect the object from the variable reference, but not when a mutating method is invoked the object.