**What does the following code return? What does it output? What concept does it demonstrate?**

```ruby
a = 4
b = 2

2.times do |a|
  a = 5
  puts a
end

puts a
puts b
```

# Written Response:

The local variable `a` is initialized and assigned to the Integer `4` on line 4. The local variable `b` is initialized and assigned to the Integer `2` on line 5. The `do...end` alongside the `times` method invocation on lines 7-10 defines a block, within which `a` attempts a reassignment to the Integer `5`; this will be ignored because of variable shadowing. In the outer scope, we have initialized the variable `a` which has the same name as our block parameter on line 7. This means the local variable `a` on line 8 never sees the initialization of variable `a` on line 4 and will be assigned to the Integer `5`; it won't be reassigned.

The `puts` method is called on line 9 and the local variable `a` is passed to it as an argument; since `a` was not reassigned inside the block; it will output the Integer `5` twice; each time on a newline. The `times` method will return the calling object; the Integer `2`.

The `puts` method is called on line 12 and the variable `a` is passed to it as an argument; since `a` was not reassigned inside the block, it will output its initialized value; the Integer `4`. The `puts` method is called on line 13 and the variable `b` is passed to it as an argument; since `b` was not reassigned anywhere in the program; it will print its initialized value; the Integer `2`.

This problem demonstrates variable shadowing. When an outer variable has the *same* name as a parameter at the method definition level; variable shadowing occurs and reassignment is ignored inside the block.

