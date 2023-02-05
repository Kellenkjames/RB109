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

The local variable `s` is initialized and assigned to the String `'hello'` on line 9. The local variable `t` is initialized and assigned to calling the `fix` method while passing `s` to it as an argument on line 10.

From within the method definition; the local variable `value` which is bound to the String `'hello'`; is reassigned on line 5; calling the `upcase` method on the original object; this returns `'HELLO'`. On line 6, the `concat` method is called on `value` with the String `('!')` passed to it as an argument; this returns `'HELLO!'`; the method returns the same value.

`s` returns the original String object; `'hello'`; since `s` was reassigned with the invocation of a non-mutating method; the original object outside the method is unchanged. `t` returns the String `'HELLO!'`; the return value of the method definition.

This problem demonstrates non-mutating methods and reassignment. Strings are mutable objects but are not always mutated when passed in as an argument to a method call. In this example, within the method; the original object was reassigned to a non-mutating method; therefore; the original object was left unchanged outside of the method definition.