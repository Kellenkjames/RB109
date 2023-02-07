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

The local variable `var` is initialized and assigned to calling the method `test`. The `test` method accepts no arguments and calls the `puts` method on line 5; while passing the String `"written assessment"` to it as an argument; the output of is the String `"written assessment"` and the return value is `nil`.

The `if...else` expressions from lines 9-13 execute a block of code; if the condition evaluates as true. The condition to be evaluated is `var`; since the return value of `test` is `nil`; and `test` is assigned to `var`; the condition evaluates as `false`.

The `else` branch of the `if...else` statement will run and calls the `puts` method on line 12 while passing the String `"interview"` in as an argument; the output is `"interview"` and the return value is `nil`.

This problem demonstrates how Ruby evaluates truthiness. In this example, the return value of the `puts` method within a method call; determines the execution of the `if...else` block. It's important to remember that with the exception of `false` and `nil`; Ruby considers everything as truthy.

