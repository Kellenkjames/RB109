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
# Written Response:

The local variable `animal` is initialized and assigned to the String `"dog"`. The `do...end` alongside the `loop` method invocation on lines 6-10 defines a block, within which `animal` is reassigned to the String `"cat"` on line 7. The local variable `var` is initialized and assigned to the String `"ball"`. The `loop` method returns `nil`.

The `puts` method is called on line 12 and the variable `animal` is passed to it as an argument; since `animal` is now the String `"cat"`; this is what is output. The `puts` method is called on line 12 has the following output: `undefined local variable or method var' for main:Object`; since `var` was initialized inside the block; it's not accessible outside of the block.

This problem demonstrates local variable scoping rules in Ruby; variables that are initialized from outside of a block are accessible inside of a block. However, when variables are initialized from inside the block, they are not accessible outside of the block.






