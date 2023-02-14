**What does the following code return? What does it output? Why? What concept does it demonstrate?**

```ruby
def fix(value)
  value << 'xyz'
  value = value.upcase
  value.concat(`!`)
end

s = 'hello'
t = fix(s)

# What values do 's' and 't' have? Why?
```
# Written Response:

The `fix` method definition accepts `value` as a parameter on line 4.

The local variable `s` is initialized and assigned to the String `'hello'` on line 10.
The local variable `t` is initialized and assigned to the `fix` method invocation passing in the reference of `s` as an argument on line 11.

Within the `fix` method body; the local variable `value` references the String `'hello'` and appends the String `'xyz'` on line 5; this returns the String `'helloxyz'`.
`value` is reassigned to invoking the `upcase` method on `self` on line 6; this returns the String `'HELLOXYZ'`.
`value` invokes the `concat` method and passes in the reference of the String literal `('!')` as an argument on line 7; the return value is the String `'HELLOXYZ!'`.

`s` now references the String `'helloxyz'`; since `s` was mutated within the `fix` method body before reassignment; `s` references the String `'helloxyz'`.
`t` now references the String `'HELLOXYZ!'`; the return value of the `fix` method invocation.

This problem demonstrates mutating methods and reassignment; specifically; what happens when a mutable object is passed to a method call as an argument and is mutated *before* reassignment. When an object is mutated before reassignment; the original object outside of the method will only be affected by mutations that occur *before* the reassignment. In this example, we can say that Ruby acts like "pass by reference".

