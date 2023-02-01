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

# Written Response

On line 4, we initialize a local variable named `a` and assign to the integer `4`.
On line 5, we initialize a local variable named `b` and assign to the integer `2`.

The `do...end` alongside the `times` method, on lines 7-10, defines a block and introduces a new scope. On line 8, we define `a` as the block parameter; the same name as the variable `a` initialized on line 5 (in the outer scope).

On line 8 `a` is initialized to the integer `5` inside the block; it is not reassigned due to variable shadowing.

The `times` method returns `2`.

On line 9, we invoke the `puts` method and pass in `a` as an argument. The output is the integer `5`; printed twice; each integer on a newline. The return value is `nil`.

On line 12, we invoke the `puts` method and pass in `a` as an argument. The output is in the integer `4`. The method returns `nil`.

On line 14, we invoke the `puts` method and pass in `b` as an argument. The output is the integer `2`. The method returns `nil`.

This problem demonstrates variable shadowing. When an outer variable in the main scope is named the same as a block parameter within a method, the variable in the inner never sees the variable in the outer scope. Therefore, re-assignment is ignored from inside the block.