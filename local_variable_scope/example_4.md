**What does the following code return? What does it output? Why? What concept does it demonstrate?**

```ruby
def example(str)
  i = 3
  loop do
    puts str
    i -= 1
    break if i == 0
  end
end

example('hello')
```

# Written Response:

On line 4, we define a method definition called `example` that accepts a string argument; `str` is the defined method parameter. On line 13, we invoke the method `example` and pass in the string `'hello'` as an argument.

On line 5, the local variable `i` is initialized and assigned to the integer `3`. The `do...end` alongside the `loop` method invocation on lines 6-10 defines a block and introduces a new scope.

On line 7, we invoke the `puts` method and pass in `str` as an argument which is bound to the string `hello` since it was passed in as an argument to the method call. On line 8, `i` uses the shorthand operator to subtract `1` from the initialized value `3` and re-assign the new value back to `i` on each iteration.

The `loop` will iterate `3` times before breaking out of the loop. The output is `'hello'` printed three times (each string on a newline) and the return value of the method is `nil`.

This problem demonstrates variable local scope rules. A method definition has it's own self-contained scope but follows the rules of variable local scope. The counter variable `i` is accessible throughout the method because it was initialized outside of the block. 

