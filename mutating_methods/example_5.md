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

The method definition `fix` accepts `value` as a parameter on line 4.

The local variable `s` is initialized and assigned to the String `'abc'` on line 9. The local variable `t` is initialized and assigned to calling the `fix` method invocation with passing `s`in as an argument on line 9.

Within the `fix` method definition; the local variable `value` references the String `'abc'` and uses an Array element setter method to assign the second index of `value` to the String `x`; this returns the String `'axc'`. `value` is referenced on line 6 which returns the String `'axc'`; this is the return value of the `fix` method invocation.

`s` returns the String `'axc'`; since `s` was mutated using an Array element setter method within the `fix` method definition; this affects the original object outside of the method.
`t` returns the String `'axc'`; the return value of the `fix` method invocation.

This problem demonstrates passing objects and mutating methods. We are most interested in whether or not the object passed into the method invocation was affected by the modifications within the method definition. In this example, an Array setter method is a mutating method that mutates an object. In this example, we can say that Ruby acts like "pass by reference".

