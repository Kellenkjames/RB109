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

The local variable `test_str` is initialized and assigned to the String `'Written Assessment'` on line 9. The method definition `test` is called on line 10 with the reference `test_str` passed to it as an argument.

The local variable `str`; which is bound to the String `'Written Assessment'`; concatenates the String `"!"` and reassigns the value back to `str` on line 5. This returns the String `'Written Assessment!'`.
The `downcase!` method is called on `str` on line 6. This returns the string `'written assessment!'` which is also the return value of the method definition `test`.

Since `test_str` is reassigned from within the method *before* a mutating method is called on the object; it returns its original object; the String `'Written Assessment'`.
The `puts` method is called with the reference `test_str` passed to it as an argument on line 11. This outputs the String `'Written Assessment'`. The method returns `nil`.

This problem demonstrates concepts of reassignment and mutating methods. When a reference is passed to a method call and the reference is reassigned *before* a mutating method is called on the object; the original object outside of the method won't be affected. Anytime a object is reassigned; the original object is disconnected from the variable.

