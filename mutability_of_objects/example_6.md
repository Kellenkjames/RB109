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

On line 9, we initialize the local variable `test_str` and assign it to the string `"Written Assessment'`. On line 10, we invoke the `test` method and pass in `test_str` as an argument.

On line 5, the local variable `str` is initialized and bound to the object `'Written Assessment'` by default as this is the object that was passed into `test` as an argument. On the same line, `str` uses the shorthand operator to concatenate `"!"` to the object `'Written Assessment'` and reassign the string; `'Written Assessment!'` back to `str`.

On line 6, we invoke the `downcase!` method (destructive) on the calling `str` object. The method returns `'written assessment!'`.

On line 11, we invoke the `puts` method and pass in `test_str` as an argument. Since we reassigned `str` on line 5; the variable changes the binding and the object the variable originally referenced it not mutated on line 6; therefore, the output is the same as the original object: `'Written Assessment`'. The method returns `nil`.

This problem demonstrates concepts of passing objects, reassignment, and mutability. In this example, we can see that strings are mutable objects and reassignment changes the binding of the variable. When a variable is reassigned before a mutating method is called on the object; it will not mutate the original object (before it was reassigned).