**What does the following code return? What does it output? Why? What concept does it demonstrate?**

```ruby
a = 4
b = 2

loop do
  c = 3
  a = c
  break
end

puts a
puts b
```
# Written Response:

The local variable `a` is initialized and assigned to the Integer `4` on line 4. The local variable `b` is initialized and assigned to the Integer `2` on line 5.

The `do...end` alongside the `loop` method invocation on lines 7-11 defines a block and introduces a new scope; within which; the local variable `c` is initialized and assigned to the Integer `3` on line 8. `a` is reassigned to `c` on line 9. The `loop` method invocation returns `nil`.

The method invocation of `puts` passes the value `a` to it as an argument on line 13. Since `a` is now assigned to `c` and `c` is assigned to the Integer `3`; this is what is output; the method returns `nil`.

The method invocation of `puts` passes the value `b` to it as an argument on line 14. Since `b` is not reassigned anywhere in the program; it will output the Integer `2`; the method returns `nil`.

This example demonstrates local variable scoping rules in Ruby; when a block is passed to a `loop` method invocation; it introduce a new scope. From inside the block, you can access variables that were initialized outside of the block. However, from outside the bock, you can't access any variables that were initialized inside the block.



