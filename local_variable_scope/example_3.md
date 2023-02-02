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

The `do...end` alongside the `loop` method invocation on lines 7-11 defines a block, which introduces a new scope. The local variable `c` is initialized and assigned to the Integer `3` on line 8. The variable `a` is reassigned to the variable `c`. The `loop` method returns `nil`.

The `puts` method is called on line 13 with the variable `a` passed to it as an argument; since the variable `a` is now assigned to the variable `c` and the variable `c` is assigned to the Integer `3`; this is what is output.

The `puts` method is called on line 14 with the variable `b` passed to it as an argument; since the variable `b` is not reassigned anywhere in the program; it will output the initialized value; `2`.

This example demonstrates local variable scoping rules in Ruby; specifically the fact that variables initialized outside of a block are accessible inside of a block.



