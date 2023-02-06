**What does the following code return? What does it output? Why? What concept does it demonstrate?**

```ruby
words = %w(jump trip laugh run talk)

new_array = words.map do |word|
  word.start_with?("t")
end

p new_array
```
# Written Response:

The local variable `words` is initialized and assigned to the Array `['jump', 'trip', 'laugh', 'run', 'talk']` on line 4. The local variable `new_array` is initialized and assigned to calling the `map` method on `words` while passing `do...end` to it as an argument; which defines a block; on lines 6-8. The parameter `word` represents the current element of `words`.

Within the block; the `start_with?` method is called on each `word` while passing the String `("t")` to it as an argument. Since the `start_with?` method checks for truthiness; it will evaluate each `word` in `words`; check which `word` starts with the String `("t")`; and return a new array of boolean objects based on truthiness; the return value is the Array `[false, true, false, false, true]`.

The `p` method is called and `new_array` is passed to it as an argument on line 10. The output is the Array `[false, true, false, false, true]` and the return value is the same object.

This problem demonstrates the behavior of the `map` method. The `map` method returns a new Array whose elements are the return values from the block. In this example, since we called the `start_with?` method on each element in the array; the return value is a *new* array of boolean objects.



