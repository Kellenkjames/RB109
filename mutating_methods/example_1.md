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

The method definition `fix` accepts `value` as a parameter on line 4. The local variable `s` is initialized and assigned to the String `'hello'` on line 10. The local variable `t` is initialized and assigned to the `fix` method invocation with passing `s` in as an argument on line 11.

Within the `fix` method definition; the local variable `value` references the String `'hello'` and invokes the `upcase!` method on `value` on line 5; this returns the String `'HELLO'`.
`value` invokes the `concat` method and passes `('!')` in as an argument on line 6; the return value is the String `'HELLO!'`.
`value` is referenced on line 7 which returns the String `'HELLO!'`; this is the return value of the `fix` method definition.

`s` returns the String `'HELLO!'`; since the original String object was mutated from within the `fix` method definition; it was changed outside of the method definition.
`t` returns the String `'HELLO!'`; this is the return value of the `fix` method definition.

This problem demonstrates passing objects and mutating methods. In this case, we can say Ruby acts as "pass by reference". When a mutable object is passed to a method via arguments and the object is mutated inside the method definition; it will change the original object outside of the method.

