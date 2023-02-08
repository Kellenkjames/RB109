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

The local variable `animal` is initialized and assigned to the String `"dog"` on line 4.

The `do...end` alongside the `loop` method invocation on lines 6-10 defines a block, within which; `animal` is reassigned to the String `"cat"` on line 7. The local variable `var` is initialized and assigned to the String `"ball"` on line 8. The `loop` method breaks on line 9 and the method invocation returns `nil`.

The method invocation of `puts` passes the reference `animal` to it as an argument on line 12. Since `animal` is now the String `"cat"`; this is what is output. The method returns `nil`.
The method invocation of `puts` passes the reference `var` to it as an argument on line 13. Since `var` was initialized from inside the block; it's not accessible outside of the block and a *error* will be thrown in the console.

This example demonstrates local variable scoping rules in Ruby; when a block is passed to a `loop` method invocation; it introduce a new scope. From inside the block, you can access variables that were initialized outside of the block. However, from outside the bock, you can't access any variables that were initialized inside the block.





