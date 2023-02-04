**What does the following code return? What does it output? Why? What concept does it demonstrate?**

```ruby
arr1 = ["a", "b", "c"]
arr2 = arr1.dup

arr2.map! do |char|
  char.upcase
end

puts arr1
puts arr2
```
# Written Response:

The local variable `arr1` is initialized and assigned to the Array `["a", "b", "c"]` on line 4. On line 5, the local variable `arr2` is initialized and assigned to the invocation of `dup` on `arr1`; this returns a shallow copy of the object.

The `do...end` alongside the `map!` invocation on `arr2` on lines 7-9 defines a block; within which `char` is assigned as the block parameter and represents the current element of `arr2` on each iteration. On each iteration, the `upcase` method is called on `char` which results in an uppercase transformation on each `char`; the method returns a new array; `["A", "B", "C"]`.

The `puts` method is called on line 11 with `arr1` passed to it as an argument; the output is the original object; `["a", "b", "c"]` and the method returns `nil`.

The `puts` method is called on line 12 with `arr2` passed to it as an argument; the output is a mutated *copy* of the original object which returns; `["A", "B", "C"]`.

This problem demonstrates the concept of reassignment and mutable objects. Arrays are mutable objects. When calling mutating methods on arrays; news objects are returned. In this example, we made a shallow copy of the original object; therefore; the original object was unchanged by the mutating method.
