**What does the following code return? What does it output? Why? What concept does it demonstrate?**

```ruby
words = %w(jump trip laugh run talk)

new_array = words.map do |word|
  word.start_with?("t")
end

p new_array
```
# Written Response:

The local variable `words` is initialized and assigned to the Array `['jump', 'trip', 'laugh', 'run', 'talk']` on line 4.
The local variable `new_array` is initialized and assigned to the `map` method invocation on the reference of `words`.

The `do...end` alongside the `map` method invocation defines a block on lines 6-8. Within the block; the parameter `word` represents the current element of `words`. The `start_with?` method invocation is called on each `word` while passing in the String literal `("t")` as an argument. Since the `start_with?` method checks for truthiness; it will evaluate each `word` in `words`; check which `word` starts with the String literal `("t")` and return a new array of boolean objects based on truthiness; this returns the following Array; `[false, true, false, false, true]`.

The `p` method invocation passes in the reference of `new_array` in as an argument on line 10; this outputs and returns the Array `[false, true, false, false, true]`.

This problem demonstrates the behavior of the `map` method. The `map` method returns a new Array whose elements are the return values from the block. In this example, since we called the `start_with?` method on each element in the array; the return value is a new array of boolean objects. The original object is left unchanged.

