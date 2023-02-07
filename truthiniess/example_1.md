**What does the following code return? What does it output? Why? What concept does it demonstrate?**

```ruby
a = "Hello"
if a
  puts "Hello is Truthy"
else
  puts "Hello is Falsey"
end
```
# Written Response:

The local variable `a` is initialized and assigned to the String `"Hello"` on line 4. The `if...else` statements executes a block of code if a specified condition is true. `a` is evaluated for truthiness on line 5; since `a` references the String `"Hello"`; this evaluates as truthy and the code within the block is executed.

Within the block; the `puts` method is called on line 6 with the String; `"Hello is Truthy"` is passed to it as an argument; the output is the String; `"Hello is Truthy"` and the return value of the method is `nil`.

This problem demonstrates how Ruby evaluates truthiness. Everything in Ruby, with the exception of `false` and `nil` is considered truthy. In addition, truthiness is not the same as the boolean object `true`. This means we can use any expression in a conditional. Expressions do not have to directly use the `true` or `false` objects.

