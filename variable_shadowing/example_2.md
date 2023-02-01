**What does the following code return? What does it output? Why? What concept does it demonstrate?**

```ruby
n = 10

1.times do |n|
  n = 11
end

puts n
```

# Written Response:

On line 4, the local variable `n` is initialized and assigned to the integer `10`. The `do...end` alongside the `times` method invocation on lines 6-8 define a block and introduces a new scope. 

On line 6, the block parameter is defined as `n`; the same variable name as `n` on line 4. Since the outer variable `n` on line 4 and the block parameter `n` on line 6 have the same name; the local variable `n` is initialized and assigned to the integer `11` on line 7; re-assignment is ignored due to variable shadowing.

The `times` method returns `1`; the calling object of the method.

On line 10, we invoke the `puts` method and pass `n` as an argument. Since `n` was never re-assigned inside the block due to variable shadowing; the output is `10`. The method returns `nil`.

This problem demonstrates the concept of variable shadowing. When a variable in the outer scope has the same name as block parameter (scoped at the method definition level), it prevents access to the outer scope variable from inside the block.

