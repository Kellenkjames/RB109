**What does the following code return? What does it output? Why? What concept does it demonstrate?**

```ruby
def a_method(string)
  string << ' world'
end

a = 'hello'
a_method(a)
p a
```
# Written Response:

The local variable `a` is initialized and assigned to the String literal `'hello'` on line 8. The `a_method` invocation passes the reference `a` as an argument on line 9.

Within the `a_method` method definition; the local variable `string` which is bound to the String literal `'hello'`; appends the String literal `' world'`; this returns the String literal `'hello world'`.

`a` returns the String literal `'hello world'` on line 8; since `a` was mutated inside the  `a_method` method definition; it affects the original object outside of the method.

`a_method(a)` returns the String literal `'hello world'`. 

The `p` method invocation passes the reference `a` as an argument on line 10; this outputs and returns the String literal `'hello world'`.

This problem demonstrates mutable objects and mutating methods. Strings are mutable objects. When an argument is passed to a method and mutated inside a method definition; it will affect the original object outside of the method.

