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

The local variable `a` is initialized and assigned to the String `'hello'` on line 8. The `a_method` is called on line 9 with `a` passed to it as an argument.

Within the method definition; the local variable `string` which is bound to the String `'hello'` appends the String `' world'`. The method returns `'hello world'`.

`a` returns the String `'hello world'` on line 8; since `a` was mutated inside the method definition; it affects the original object outside of the method.

The `a_method` is called on line 9 with `a` passed to it as an argument; the return value is `'hello world'`.

The `p` method is called on line 10 while passing `a` to it as an argument; the method prints and returns the same value; `'hello world'`.

This problem demonstrates mutable objects and mutating methods. Strings are mutable objects. When an argument is passed to a method and mutated inside a method definition; it will affect the original object outside of the method.

