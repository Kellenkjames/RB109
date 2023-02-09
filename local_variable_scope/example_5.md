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

The method definition `greetings` accepts `str` as a parameter on line 4.

The local variable `word` is initialized and assigned to the String `"Hello"` on line 9. The `greetings` method invocation passes the reference `word` to it as an argument on line 10.

The `puts` method invocation passes the reference `str` as an argument on line 5. `str` represents a local variable and is bound to the String `"Hello"`; this is what is output.

The `puts` method invocation passes the reference `"Goodbye"` as an argument on line 6. Since the argument is the String `"Goodbye"`; this is what is output.

The `greetings` method invocation returns `nil`. Ruby methods always return the evaluated result of the last line of the expression; unless an explicit return comes before it; since the expression of the last line is the `puts` method invocation with no explicit return statements before it; the return value of the `greetings` method invocation is `nil`.

This problem demonstrates local variable scope rules in Ruby; specifically when there is data outside of a method definition's scope, the data has to be passed into the method via arguments in order for the method to have access.


