**What does the following code return? What does it output? Why? What concept does it demonstrate?**

```ruby
animal = "dog"

loop do |_|
  animal = "cat"
  var = "ball"
  break
end

puts animal
puts var
```

On line 4, the local variable `animal` is initialized and assigned to the string `"dog"`. The `do...end` alongside the `loop` method invocation on lines 6-10 defines a block and introduces a new scope.

On line 7, `animal` is re-assigned to the string `"cat"`. On line 8, the local variable `var` is initialized and assigned to the string `"ball"`. The `loop` method returns `nil`.

On line 12, we invoke the `puts` method and pass in `animal` as an argument. Since `animal` was re-assigned to the string `"cat"` on line 7; this is the output. The method returns `nil`.

On line 13, we invoke the `puts` method and pass in `var` as an argument. Since `var` was initialized inside the block, we get the following error: `undefined local variable or method 'var' for main:Object`. This means `var` is not accessible from outside the block since it was initialized from inside the block.

This problem demonstrates variable local scoping rules. With blocks, inner scope can access variables initialized in an outer scope, but not vice versa.




