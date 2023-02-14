**What does the following code return? What does it output? Why? What concept does it demonstrate?**

```ruby
def fix(value)
  value = value.upcase
  value.concat('!')
end

s = 'hello'
t = fix(s)

# What values do `s` and `t` have? Why?
```
# Written Response:

The `fix` method definition accepts `value` as a parameter on line 4.

The local variable `s` is initialized and assigned to the String `'hello'` on line 9.
The local variable `t` is initialized and assigned to the `fix` method invocation passing in the reference of `s` as an argument on line 10.

Within the `fix` method body; the local variable `value` which references the String `'hello'`; is reassigned to the method invocation of `upcase` on `self`; this returns the String `'HELLO'` on line 5.
`value` invokes the `concat` method with passing in the reference of the String literal `('!')` as an argument; this returns the String `'HELLO!'` on line 6.

`s` still references the original String `'hello'`; since `s` is reassigned within the `fix` method body; the original object outside the method is left unchanged.
`t` now references the String `'HELLO!"`; the return value of the `fix` method invocation.

This problem demonstrates object passing and non-mutating methods. When an object is passed into a method as an argument and reassigned within the method definition; the original object outside the method is left unchanged. Reassignment never mutates a method.


