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

The local variable `a` is initialized and assigned to the String `'hello'` on line 8. The `a_method` invocation passes `a` in as an argument on line 9.

Within the `a_method` method definition; the local variable `string` references the String `'hello'` and appends the String `' world'`; this returns the String `'hello world'`; the `a_method` definition returns the same value.

`a` returns the String `'hello world'`; since `a` was mutated inside the  `a_method` method definition; it affects the original object outside of the method.
The `p` method invocation passes `a` in as an argument on line 10; this outputs and returns the String `'hello world'`.

This problem demonstrates object passing and mutating methods. When passing a mutable object to a method invocation and mutating the object from within the method; this will affect the original object outside of the method. In this example, we can say Ruby acts as "pass by reference."

