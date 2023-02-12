**What does the following code return? What does it output? Why? What concept does it demonstrate?**

```ruby
def test
  puts "written assessment"
end

var = test
if var
  puts "written assessment"
else
  puts "interview"
end
```
# Written Response:

The `test` method definition accepts no parameters on line 4. The local variable `var` is assigned and initialized to the `test` method invocation on line 8.
The `if...else` statement on lines 9-13 will execute the code for the first expression that evaluates as true.

`var` is checked for truthiness on line 9. Since `var` is assigned to the return value of `test` and the `return` value of `test` is `nil`; this expression evaluates as false; therefore, the code within the `if` statement will be ignored.

The code on line 12 will be evaluated; the `puts` method invocation passes in the String `"interview"`; this outputs the String `"interview"` and returns `nil`.

This problem demonstrates how Ruby evaluates for truthiness. Everything in Ruby with the exception of `false` and `nil` is considered truthy. Truthiness allows Ruby to evaluate any expression in a conditional statement without the object having to be equal to the booleans `true` or `false`.

