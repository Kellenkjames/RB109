**What does the following code return? What does it output? Why? What concept does it demonstrate?**

```ruby
def fix(value)
  value = value.upcase!
  value.concat('!')
end

s = 'hello'
t = fix(s)

# What values do `s` and `t` have? Why?
```
# Written Response:

The local variable `s` is initialized and assigned to the String literal `'hello'` on line 9. The local variable `t` is initialized and assigned to the `fix` method invocation with the reference `s` passed as an argument on line 10.

Within `fix` the method definition; the local variable `value` which is bound to the String `'hello'`; is reassigned to the `upcase!` method invocation; this returns the String literal `'HELLO'`.
The `concat` method is invoked on `value` while the reference `('!')` is passed as an argument; this returns the String literal `'HELLO!'`.

`s` returns the String literal; `HELLO!`; Since `s` is mutated within the `fix` method definition; the object outside of the method is affected.
`t` returns the String literal `'HELLO!'`; the return value of the `fix` method invocation.

This problem demonstrates mutating methods and reassignment. When a mutating method is called on an object and reassigned *back to itself*; it does not create a new variable reference or binding. The calling object is mutated and the original object outside of the method definition will be affected.