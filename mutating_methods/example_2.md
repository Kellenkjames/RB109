**What does the following code return? What does it output? Why? What concept does it demonstrate?**

```ruby
def fix(value)
  value = value.upcase # reassignment with a non-mutating method will not affect the object outside the method.
  value.concat('!')
end

s = 'hello'
t = fix(s)

# What values do `s` and `t` have? Why?
```
# Written Response:

The local variable `s` is initialized and assigned to the String literal `'hello'` on line 9. The local variable `t` is initialized and assigned to the `fix` method invocation with passing the reference `s` as an argument on line 9.

Within the `fix` method definition; the local variable `value` which is bound to the String `'hello'`; is reassigned to the invocation of the `upcase` method on `value`; this returns the String literal `'HELLO'`.The`concat` method is invoked on `value` with the reference `('!')` passed to it as an argument; this returns the String literal `'HELLO!'`; the `fix` method invocation returns the same value.

`s` returns the original String object; `'hello'`; since `s` is reassigned with a non-mutating method within the `fix` method definition; the original object outside the method is not affected.
`t` returns the String `'HELLO!'`; the return value of the `fix` method invocation.

This problem demonstrates non-mutating methods and reassignment. Strings are mutable objects but are not always mutated when passed in as an argument to a method call. In this example, within the method; the original object was reassigned to a non-mutating method; therefore; the original object was left unchanged outside of the method definition.

