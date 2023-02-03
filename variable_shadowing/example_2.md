**What does the following code return? What does it output? Why? What concept does it demonstrate?**

```ruby
n = 10

1.times do |n|
  n = 11
end

puts n
```

# Written Response:

The local variable `n` is initialized and assigned to the Integer `10`. The `do...end` alongside the `times` method invocation on lines 6-8 defines a block, within which the variable `n` attempts reassignment to the Integer `11`; this will be ignored because of variable shadowing. The outer variable `n` on line 4 has the *same* name as the block parameter on line 6; therefore; the local variable `n` on line 7 never sees the initialization of variable `n` on line 4 and will be assigned to the Integer `11`.

The return value of the `times` method is the calling object; the Integer `1`. The `puts` method is called on line 10 and the variable `n` is passed to it as an argument; since the variable `n` was not reassigned inside the block; it will output its initialized value; `10`.

