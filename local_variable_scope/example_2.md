**What does the following code return? What does it output? Why? What concept does it demonstrate?**

```ruby
a = 4

loop do
  a = 5
  b = 3

  break
end

puts a
puts b
```
# Written Response:

The local variable `a` is initialized and assigned to the Integer `4` on line 4. The `do...end` alongside the `loop` method invocation on lines 6-11 defines a block and introduces a new scope; within which; `a` is reassigned to the Integer `5` on line 7. The local variable `b` is initialized and assigned to the Integer `3` on line 8. The `loop` method invocation returns `nil`.

The method invocation of `puts` passes the value `a` to it as an argument. Since `a` is now assigned to the Integer `5`; this is what is output; the method returns `nil`.

The method invocation of `puts` passes the value `b` to it as an argument. Since `b` was initialized from inside of the block; it's not accessible from outside of the block; therefore; a *NameError* will be thrown in the console.

This example demonstrates local variable scoping rules in Ruby; when a block is passed to a `loop` method invocation; it introduce a new scope. From inside the block, you can access variables that were initialized outside of the block. However, from outside the bock, you can't access any variables that were initialized inside the block.



