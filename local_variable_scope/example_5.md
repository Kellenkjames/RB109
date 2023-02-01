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

On line 4, we define a method called `greetings` that accepts one argument as input. `str` is  defined as the method parameter.

On line 9, the local variable `word` is initialized and assigned to the string `"Hello"`. On line 10, we invoke the method `greetings` and pass in `word` as an argument.

On line 5, we invoke the `puts` method and pass in `str` as an argument; `str` is bound to the string `"Hello"` since it was passed in as an argument to the method invocation of `greetings`; therefore, the output is the string `"Hello"`. The method returns `nil`.

On line 6, we invoke the `puts` method and pass in the string literal `"Goodbye"` as an argument; this is the output. The method returns `nil`.

The return value of the `greetings` method is `nil`.

This problem demonstrates variable local scope rules. In Ruby, methods have their own-self contained scope. Methods can't access any variables outside of the method definition unless data is passed into the method invocation as an argument.





