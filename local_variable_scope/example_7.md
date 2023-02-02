**What does the following code return? What does it output? Why? What concept does it demonstrate?**

```ruby
a = 'Bob'

5.times do |x|
  a = 'Bill'
end

p a
```
# Written Response:

The local variable `a` is initialized and assigned to the String `'Bob'` on line 4. The `do...end` alongside the `times` method invocation on lines 6-8 defines a block, within which `a` is reassigned to the String `'Bill'`. The `times` method iterates over the given block, passing in increasing values from the Integer `0` up to the calling object; `5` minus `1`; represented by the block parameter `x`. This results in `a` being reassigned to the String `"Bill"` a total of `5` times. The method returns the calling object; the Integer `5`.

The `p` method is called on line 10 and the variable `a` passed to it as an argument; since `a` is now the String `Bill`; this is the output and the return value of the `p` method.


