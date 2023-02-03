**What does the following code return? What does it output? Why? What concept does it demonstrate?**

```ruby
animal = "dog"

loop do |animal|
  animal = "cat"
  break
end

puts animal
```

# Written Response:

The local variable `animal` is initialized and assigned to the String `"dog"`. The `do...end` alongside the `loop` method invocation defines a block from lines 6-9, within which `animal` attempts reassignment to the String `"cat"`; this is ignored due to variable shadowing. The outer variable `animal` on line 4 is named the *same* as the block parameter on line 6; therefore; the local variable `animal` on line 7 never sees the initialization of the outer variable and assigns the String `"cat"`. The `loop` method returns `nil`.

The `puts` method is called on line 11 and the variable `animal` is passed to it as an argument; since `animal` was not reassigned inside the block; the output will be the initialized value of `animal` on line 4; `"dog"`. 