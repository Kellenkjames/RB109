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

The local variable `a` is initialized and assigned to the Integer `4` on line 4.
The local variable `b` is initialized and assigned to the Integer `2` on line 5.

The `do...end` alongside the `times` method invocation defines a block from lines 7-10. Within the block; `a` is defined as the parameter and represents the current iteration of the `times` method starting from the Integer `0`. The local variable `a` is initialized and assigned to the Integer `5` on line 8. The `puts` method invocation passes in the reference of `a` in as an argument on line 9; this outputs the Integer `5`; two times each on a newline.

The `times` method invocation returns the calling object; the Integer `2`.

The `puts` method invocation passes in the reference of `a` in as an argument on line 12. Since `a` was not reassigned within the block; it will output its original object; the Integer `4`. The `puts` method invocation passes in the reference of `b` in as an argument on line 13. Since `b` was not reassigned anywhere in the program; it will output its original object; the Integer `2`.

This problem demonstrates variable shadowing. When a block parameter has been defined with the same name as a variable in the outer scope; reassignment will be ignored inside the block due. Variable shadowing prevents the inner scoped variable from accessing the outer scope variable.

