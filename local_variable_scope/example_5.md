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

The local variable `word` is initialized and assigned to the String `"Hello"` on line 9. The method invocation of `greetings` passes the reference `word` to it as an argument on line 10.

The method invocation of `puts` passes the reference `str` to it as an argument on line 5; since `str` is bound to the String `"Hello"`; this is what is output.

The method invocation of `puts` passes the String literal `"Goodbye"` to it as an argument on line 6; since the argument is the String literal `"Goodbye"`; this is what is output.

Ruby methods always return the evaluated result of the last line of the expression; unless an explicit return comes before it; since the expression of the last line is the invocation of the`puts` method with no explicit return statements before it; the return value of the method definition `greetings` is `nil`.

This problem demonstrates local variable scope rules in Ruby; specifically when there is data outside of a method definition's scope, the data has to be passed into the method via arguments in order for the method to have access.



