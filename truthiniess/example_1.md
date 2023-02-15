**What does the following code return? What does it output? Why? What concept does it demonstrate?**

```ruby
a = "Hello"
if a
  puts "Hello is Truthy"
else
  puts "Hello is Falsey"
end
```
# Written Response:

The local variable `a` is initialized and assigned to the String `"Hello"` on line 4. The `if...else` conditional statement on lines 5-9 checks if `a` evaluates to true; false otherwise. Since `a` is assigned to the String `"Hello"`; this evaluates to true.

The code within the `if` block statement will execute. The `puts` method invocation passing in the String `"Hello is Truthy"` as an argument; this outputs the String `"Hello is Truthy"` and returns `nil`.

This problem demonstrates how Ruby evaluates for truthiness. Everything in Ruby with the exception of `false` and `nil` is considered truthy. Truthiness allows Ruby to evaluate any expression in a conditional statement without the object having to be equal to the booleans `true` or `false`.

