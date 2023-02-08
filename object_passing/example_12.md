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

The local variable `arr1` is initialized and assigned to the Array literal `["a", "b", "c"]` on line 4. The local variable `arr2` is initialized and assigned `arr1` invoking the `dup` method on line 5; this returns a shallow copy of the original object; `["a", "b", "c"]`.

The `do...end` alongside the `map!` invocation on lines 7-9 defines a block; within which; `char` is assigned as the block parameter and represents the current element of `arr2`; the shallow copy of the original object. On each iteration, the `upcase` method is called on `char` which results in an uppercase transformation of each `char` in `arr2`; the method returns a new array; `["A", "B", "C"]`.

The `puts` method invocation passes the reference `arr1` as an argument on line 11; this outputs each String literal of the Array literal `["a", "b", "c"]` on a newline and the method returns `nil`.

The `puts` method invocation passes the reference `arr2` as an argument on line 12. Since `arr2` is mutated; this outputs each String literal of the Array literal `["A", "B", "C"]` on a newline and the method returns `nil`.

This problem demonstrates the concept of reassignment and mutable objects. Arrays are mutable objects. When calling mutating methods on arrays; *new* objects are returned; however; in this example, the mutating method was invoked on a shallow copy of the original object; therefore; the original object is left *unchanged*.
