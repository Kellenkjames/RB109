**What does the following code return? What does it output? Why? What concept does it demonstrate?**

```ruby
odd, even = [1, 2, 3].partition do |num|
  num.odd?
end

p odd
p even
```
# Written Response:

The local variables `odd, even` are initialized and assigned to the Array `[1, 2, 3]`. The `do...end` alongside the `partition` method on lines 4-6 defines a block; while the block parameter `num` represents the current element of the Array.

Within the block; `num.odd?` will return the following partition: `[1, 3], [2]`; this is the return value of the method.

The `p` method is called with the variable `odd` passed to it as an argument; this outputs `[1, 3]` and returns the same value.

The `p` method is called with the variable `even` passed to it as an argument; this outputs `[2]` and returns the same value.

This problem demonstrates multiple assignments in a single operation as well as the `partition` method in Ruby. The `partition` method with a given block, returns an array of two arrays; the first having those elements for which the block returns a truthy value; the other over having all other elements.