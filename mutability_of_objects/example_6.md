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

The local variable `test_str` is initialized and assigned to the String `'Written Assessment'` on line 9. The `test` method is called on line 10 with `test_str` passed to it as an argument.

The local variable `str` which is bound to the String `Written Assessment` uses shorthand reassignment to perform the following operation: `Written Assessment` + `"!"` and stores the value back to `str` on line 5.

`str` is now the String `'Written Assessment!'` and the `downcase!` method is called on the object on line 6.

The method returns `'written assessment!`. The `puts` method is called on line 11 and the variable `test_str` is passed to it as an argument; since `test_str` was reassigned in the method before it was mutated; the output is the original String; `Written Assessment`.

