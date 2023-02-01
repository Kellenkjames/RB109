**What does the following code return? What does it output? Why? What concept does it demonstrate?**

```ruby
a = 'Bob'

5.times do |x|
  a = 'Bill'
end

p a
```

On line 4, the local variable `a` is initialized and assigned to the string `'Bob'`. The `do...end` alongside the `times` method invocation on lines 6-8 defines a block and introduces a new scope.

On line 7, `a` is re-assigned to the string `'Bill'`. Since `a` is re-assigned within the `times` method and `5` is the calling object; `a` is re-assigned to `Bill` a total of `5 ` times. The method returns `5`.

On line 10, we invoke the `p` method and pass in `a` as an argument. Since `a` was re-assigned to the string `'Bill'`; this is the output. The `p` method returns the string `'Bill'`.

This problem demonstrates variable local scoping rules. With blocks, inner scope can access variables initialized in an outer scope, but not vice versa. These scoping rules apply as long as block immediately follows a method invocation. 
