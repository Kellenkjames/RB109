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

The local variable `animal` is initialized and assigned to the String `"dog"` on line 4.

The `do...end` alongside the `loop` method invocation defines a block from lines 6-9. Within the block, `animal` is defined as the parameter. The loop iterates once and within the iteration; the local variable `animal` is initialized and assigned to the String `"cat"`. The `loop` method invocation returns `nil`.

The `puts` method invocation passed in the reference of `animal` in as an argument on 11; this outputs the String `"dog"` and returns `nil.`.

This problem demonstrates variable shadowing. When a block parameter has the same name as a variable in the outer scope; the inner scope variable cannot access the variable in the outer scope.