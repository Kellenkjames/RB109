**What does the following code return? What does it output? Why? What concept does it demonstrate?**

```ruby
n = 10

1.times do |n|
  n = 11
end

puts n
```

# Written Response:

The local variable `n` is initialized and assigned to the Integer `10`.

The `do...end` alongside the `times` method invocation defines a block from lines 6-8. Within the block; the parameter `n` represents the current iteration of the `times` method. The loop will iterate once and initialize and assign the local variable `n` to the Integer `11`.

The `times` method invocation returns the calling object; the Integer `1`.

The `puts` method invocation passes in the reference of `n` as an argument on line 10. Since `n` was not reassigned within the block; it outputs its original object; the Integer `10` and returns `nil`.

This problem demonstrates variable shadowing. When a block parameter is defined and named the same as a variable in the outer scope; the inner scope variable cannot access the variable in the outer scope.




