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

The local variable `a` is initialized and assigned to the Integer `4` on line 4. The `do...end` alongside the `loop` method invocation on lines 6-11 defines a block, which introduces a new scope and within which; `a` is reassigned to the Integer `5` on line 7. The local variable `b` is initialized and assigned to the Integer `3` on line 8. The `loop` method returns `nil`.

The `puts` method is called on line 13 with the value `a` passed to it as an argument; since `a` is now assigned to the Integer `5`; this is what is output. The method returns `nil`.

When calling the `puts` method on line 14, an error is thrown in the terminal; since we initialized `b` from within the block; `b` is not accessible from outside the block.

This example demonstrates local variable scoping rules in Ruby; when a block is passed to a `loop` method; it introduce a new scope. From inside the block, you can access variables that were initialized outside of the block. However, from outside the bock, you can't access any variables that were initialized inside the block.



