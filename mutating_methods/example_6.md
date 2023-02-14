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

The `a_method` method definition accepts `string` as a parameter on line 4.

The local variable `a` is initialized and assigned to the String `'hello'` on line 8.
The `a_method` invocation passes in the reference of `a` as an argument on line 9.

Within the `a_method` method body; the local variable `string` references the String `'hello'` and appends the String `' world'`; this returns the String `'hello world'`.

`a` now references the String `'hello world'`; since `a` was mutated within the `a_method` method body; this affects the original object outside of the method.
The `p` method invocation passes in the reference of `a` as an argument on line 10; this outputs and returns the String `'hello world'`.

This problem demonstrates object passing and mutating methods. When passing a mutable object as an argument to a method and mutating the object from within the method body; this will affect the original object outside of the method. In this example, we can say Ruby acts like "pass by reference."

