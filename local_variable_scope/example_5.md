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

The local variable `word` is initialized and assigned to the String `"Hello"` on line 9. The method `greetings` is called on line 10 with the variable `word` passed to it as an argument.

The `puts` method is called on line 5 with the local variable `str` passed to it as an argument; since the local variable `str` is bound to the String `"Hello"`; this is what is output. The `puts` method is called on line 6 with the String literal `"Goodbye"` passed to it as an argument; since the argument is the String literal `"Goodbye"`; this is what is output.

This problem demonstrates local variable scope rules in Ruby; When there is data outside of a method definition's scope, the data has to be passed in via arguments to access it within the method definition.

