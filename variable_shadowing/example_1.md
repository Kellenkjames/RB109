
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

On line 5, we initialize a local variable named `a` and assign to the integer `4`. On line 6, we initialize a local variable named `b` and assign to the integer `2`.

The `do...end` alongside the `times` method, on lines 8-11, defines a block and introduces a new scope. On line 8, we assign `a` as the name of our block parameter; the same name as the variable `a` initialized on line 5.

On line 9 `a` is initialized to the integer `5` inside the block; it is not reassigned to the outer variable `a`; the outer variable `a` is ignored due to variable shadowing.

The return value of the `times` method is `2`. The `times` method returns `self`; which in this case, is the calling object; the integer `2`.

On line 10, we invoke the `puts` method and pass in `a` as an argument. The output is the integer `5` twice (each on a newline) and the return value is `nil`.

On line 13, we invoke the `puts` method and pass in `a` as an argument. The output is in the integer `4`. `a` is never reassigned inside of the block due to variable shadowing; therefore, it will output its initialized value from line 5. The return value of the `puts` method is `nil`.

On line 14, we invoke the `puts` method and pass in `b` as an argument. The output is the integer `2`. `b` is never reassigned in the program; therefore, it will output its original initialized value on line 6; `2`. 

This problem demonstrates variable shadowing. When an outer variable in the main scope is named the same as a block parameter within a method; it prevents access to the outer scope local variable.