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

The local variable `test_str` is initialized and assigned to the String literal `'Written Assessment'` on line 9. The `test` method invocation passes the reference `test_str` as an argument on line 10.

The local variable `str`; which is bound to the String literal `'Written Assessment'`; concatenates the String literal `"!"` and reassigns the value back to `str` on line 5; this returns the String literal `'Written Assessment!'`.

`str` invokes the `downcase!` method on line 6.; this returns the String literal `'written assessment!'` which is the return value of the `test` method invocation.

Since `test_str` is reassigned from within the method *before* a mutating method is called on the object; it returns its original object; the String literal `'Written Assessment'`.

The `puts` method invocation passes the reference `test_str` as an argument on line 11; this outputs the String literal `'Written Assessment'` and the method returns `nil`.

This problem demonstrates concepts of reassignment and mutating methods. When a reference is passed to a method call and the reference is reassigned *before* a mutating method is called on the object; the original object outside of the method won't be affected. Anytime a object is reassigned; the original object is disconnected from the variable.

