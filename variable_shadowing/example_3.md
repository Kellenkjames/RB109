**What does the following code return? What does it output? Why? What concept does it demonstrate?**

```ruby
animal = "dog"

loop do |animal|
  animal = "cat"
  break
end

puts animal
```

# Written Response:

On line 4, the local variable `animal` is initialized and assigned to the string `"dog"`. The `do...end` alongside the `loop` method invocation on lines 6-9 define a block and introduces a new scope.

On line 6, `animal` is defined as the block parameter; the same name as the outer variable on line 4. On line 7, the local variable `animal` is initialized and assigned to the string `"cat"`;re-assignment is ignored due to variable shadowing.

The `loop` method returns `nil`.

On line 11, we invoke the `puts` method and pass in `animal` as an argument. Since `animal` was never re-assigned inside the block due to variable shadowing; the output is the string `"dog"`. The method returns `nil`.

This problem demonstrates the concept of variable shadowing. Although a uncommon use case; `loop` methods can accept a block parameter. If the block parameter is the named the same as a variable in the outer scope; the variable in the outer scope will be ignored from inside the block.