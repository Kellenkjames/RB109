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

The `fix` method definition accepts `value` as a parameter on line 4.

The local variable `s` is initialized and assigned to the String `'abc'` on line 9. The local variable `t` is initialized and assigned to the `fix` method invocation passing in `s` as an argument on line 9.

Within the `fix` method body; the local variable `value` references the String `'abc'` and uses the element assignment method to assign the second index of `value` to the String `'x'`; this returns the String `'axc'`. `value` is referenced on line 6 which points to the String `'axc'`.

`s` now references the String `'axc'`; since `s` was mutated using an element assignment method within the `fix` method body; this affects the original object outside of the method.
`t` now references the String `'axc'`; the return value of the `fix` method invocation.

This problem demonstrates passing objects and mutating methods. We are most interested in whether or not the object passed into the method invocation was affected by the operations or methods within the method body. In this example, an element assignment method is a mutating operation that mutates an object. In this example, we can say that Ruby acts like "pass by reference".

