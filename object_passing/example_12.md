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

The local variable `arr1` is initialized and assigned to the Array `["a", "b", "c"]` on line 4.
The local variable `arr2` is initialized and assigned the method invocation of `dup` on `arr1`; this returns a shallow copy of the original object; `["a", "b", "c"]`.

The `do...end` alongside the `map!` invocation on lines 7-9 defines a block; within which; `char` is assigned as the block parameter and represents the current element of `arr2`; the shallow copy of the original object. On each iteration, the `upcase` method is invoked on `char` which results in an uppercase transformation of each `char` in `arr2`; the method returns a new array; `["A", "B", "C"]`.

The `puts` method invocation passes in the reference of `arr1` as an argument on line 11; Since `arr1` was not mutated by the method invocation of `map!`; this outputs each String of the Array `["a", "b", "c"]` on a newline and the method returns `nil`. The `puts` method invocation passes in the reference of `arr2` as an argument on line 12. Since `arr2` was mutated; this outputs each String of the Array `["A", "B", "C"]` on a newline and the method returns `nil`.

This problem demonstrates mutating methods. When invoking a mutating method on an object; any variable referencing that object will be affected. In this example, the mutating method was invoked on a *shallow* copy of the original object; therefore; the original object was left unchanged.

