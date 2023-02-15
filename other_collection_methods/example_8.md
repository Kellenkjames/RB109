**What does the following code return? What does it output? Why? What concept does it demonstrate?**

```ruby
odd, even = [1, 2, 3].partition do |num|
  num.odd?
end

p odd
p even
```
# Written Response:

The local variables `odd, even` are initialized and assigned to the Array literal `[1, 2, 3]`.
The `do...end` alongside the `partition` method on lines 4-6 defines a block; while the block parameter `num` represents the current element of the Array.

Within the block; `num.odd?` is called on each Array element and returns the following Array literal: `[[1, 3], [2]]`.

The `p` method invocation passes in the reference of `odd` as an argument; this outputs and returns the Array literal `[1, 3]`.
The `p` method invocation passes in the reference of `even` as an argument; this outputs and returns the Array literal `[2]`.

This problem demonstrates multiple assignments in a single operation as well as the `partition` method in Ruby. The `partition` method with a given block, returns an array of two arrays; the first having those elements for which the block returns a truthy value; the other over having all other elements.