**What does the following code return? What does it output? Why? What concept does it demonstrate?**

```ruby
def greetings(str)
  puts str
  puts "Goodbye"
end

word = "Hello"
greetings(word)
```
# Written Response:

The `greetings` method definition accepts `str` as a parameter on line 4.

The local variable `word` is initialized and assigned to the String `"Hello"` on line 9.
The `greetings` method invocation passes in the reference of `word` as an argument on line 10.

The `puts` method invocation passes in the reference of `str` as an argument which is the String `"Hello"` on line 5; this is what is output.
The `puts` method invocation passes in the String literal `"Goodbye"` as an argument on line 6; this is what is output.

Since the reference of `word` was not mutated within the `greetings` method body; `word` references the original String object `"Hello"`.
The `greetings` method invocation returns `nil`.

This problem demonstrates local variable scope rules in Ruby. Methods have their own self-contained scope. When there is data outside of a method definition's scope, it must be passed into the method via arguments in order to be modified or used to return a specific result.