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

The `fix` method definition accepts `value` as a parameter on line 4.

The local variable `s` is initialized and assigned to the String `'hello'` on line 9.
The local variable `t` is initialized and assigned to the `fix` method invocation passing in `s` in as an argument on line 10.

Within the `fix` the method body; the local variable `value` references the String `'hello'` and is reassigned to the `upcase!` method invocation on `self`; this returns the String `'HELLO'`.
`value` invokes the `concat` method and passes in the reference of the String literal `('!')` as an argument; this returns the String `'HELLO!'`.

`s` now references the String `'HELLO!'`; since the original String object was mutated from within the `fix` method body; it was changed outside of the method.
`t` now references the return value of the `fix` method invocation which is the String `'HELLO!'`.

This problem demonstrates object passing and mutating methods; specifically; reassigning an object to a mutating method. When a mutable object is passed into a method invocation and the object is reassigned to mutating method; it will affect the original object outside of the method. In this example, we can say that Ruby acts like "pass by reference."