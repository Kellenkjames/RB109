**What does the following code return? What does it output? Why? What concept does it demonstrate?**

```ruby
a = 'Bob'

5.times do |x|
  a = 'Bill'
end

p a
```
# Written Response:

The local variable `a` is initialized and assigned to the String `'Bob'` on line 4.

The `do...end` alongside the `times` method invocation on lines 6-8 defines a block and introduces a new scope, within which; `a` is reassigned to the String `'Bill'`. The `times` method iterates over the given block starting from the Integer `0` up to the calling object; the Integer `5` minus the Integer `1`. This results in `a` being reassigned to the String `"Bill"` the Integer `5` times. The `times` method invocation returns the calling object; the Integer `5`.

The `p` method invocation passes `a` in as an argument on line 10; this outputs and returns the String `'Bill'`.

This example demonstrates local variable scoping rules in Ruby; when a block is passed to a `times` method invocation; it introduce a new scope. From inside the block, you can access variables that were initialized outside of the block. However, from outside the bock, you can't access any variables that were initialized inside the block.