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

The `fix` method definition accepts `value` as a parameter on line 4.
The local variable `s` is initialized and assigned to the String `'hello'` on line 10.
The local variable `t` is initialized and assigned to the `fix` method invocation passing in the reference of `s` as an argument on line 11.

Within the `fix` method body; the local variable `value` references the String `'hello'` and invokes the `upcase!` method on line 5; this returns the String `'HELLO'`.
`value` invokes the `concat` method and passes in the reference of the String literal `('!')` as an argument on line 6; this returns the String `'HELLO!'`.
`value` is referenced on line 7 which points to the String `'HELLO!'`; this is the return value of the `fix` method definition.

`s` now references the String `'HELLO!'`; since the original String object was mutated from within the `fix` method body; it was changed outside of the method.
`t` now references the String `'HELLO!'`; the return value of the `fix` method invocation.

This problem demonstrates passing objects and mutating methods. When a mutable object is passed to a method via arguments and the object is mutated inside the method definition; it will change the original object outside of the method. In this case, we can say Ruby acts like "pass by reference".