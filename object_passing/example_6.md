**What does the following code return? What does it output? Why? What concept does it demonstrate?**

```ruby
def test(str)
  str += "!"
  str.downcase!
end

test_str = 'Written Assessment'
test(test_str)
puts test_str
```
# Written Response:

The method definition `test` accepts `str` as a parameter on line 4.

The local variable `test_str` is initialized and assigned to the String `'Written Assessment'` on line 9. The `test` method invocation passes `test_str` in as an argument on line 10.

Within the `test` method definition; the local variable `str`; which references `test_str` on line 9; concatenates the String `"!"` and reassigns the value back to `str` on line 5; this returns the String `'Written Assessment!'`. `str` invokes the `downcase!` method on line 6; this returns the String `'written assessment!'`; which is the return value of the `test` method invocation.

Since `test_str` is reassigned from within the method *before* a mutating method is called on the object; it returns its original object; the String `'Written Assessment'`.
The `puts` method invocation passes `test_str` in as an argument on line 11; this outputs the String `'Written Assessment'` and the method returns `nil`.

This problem demonstrates reassignment and mutable objects. When an object is passed to a method and it is reassigned before a mutating method is called upon it; the original object outside the method is unchanged. Reassignment breaks the connection to the original object and binds the variable to a new object.

