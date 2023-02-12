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

The local variable `a` is initialized and assigned to the String `"Hello"` on line 4. The `if...else` statement on lines 5-9 will execute the code for the first statement that evaluates as truthy. `a` is checked for truthiness on line 5. Since `a` is assigned to a String `"Hello"`; this evaluates as truthy. 

The code within the `if` statement will execute which results in the `puts` method invocation passing in the String `"Hello is Truthy"` as an argument; this outputs the String `"Hello is Truthy"` and returns `nil`.

This problem demonstrates how Ruby evaluates for truthiness. Everything in Ruby with the exception of `false` and `nil` evaluates as truthy. Truthiness allows Ruby to evaluate any expression in a conditional statement without the object having to be equal to the booleans `true` or `false`.

