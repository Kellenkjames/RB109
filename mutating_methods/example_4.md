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

The local variable `s` is initialized and assigned to the String `'hello'` on line 9. The local variable `t` is initialized and assigned to calling the `fix` method while passing `s` to it as an argument; on line 10.

Within the method definition; the local variable `value` which is bound to the String `'hello'` is reassigned to `value.upcase!` on line 5. On line 6, the `concat` method is called on `value` while the String `('!')` is passed to it as an argument. The return value of the method is the String `'HELLO!'`.

The variable `s` returns the String `'HELLO!'`; since `s` was mutated within the method definition and reassigned back to the same variable; it affected the original object outside of the method definition.

The variable `t` returns the String `'HELLO!'`; the return value of the method definition.

This problem demonstrates mutating methods and reassignment. When a mutating method is called on an object and reassigned *back to itself*; it does not create a new variable reference or binding. The calling object is mutated and the original object outside of the method definition will be affected.