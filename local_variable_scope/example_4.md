**What does the following code return? What does it output? Why? What concept does it demonstrate?**

```ruby
def example(str)
  i = 3
  loop do
    puts str
    i -= 1
    break if i == 0
  end
end

example('hello')
```
# Written Response:

The method definition `example` is called on line 13 with the String `'hello'` passed to it as an argument. The local variable `i` is initialized and assigned to the Integer `3` on line 5. The `do...end` alongside the `loop` method invocation on lines 6-10 defines a block, within which; the `puts` method is called with the value `str`; which is bound to the String `'hello'`; is passed to it as an argument. The output is the String `'hello'`; which prints on a newline; three times.

Within the `loop` method; `i` subtracts the Integer `1` and reassigns the value back to `i` on line 8. The `loop` method will break if `i` is equal to the Integer `0`; as shown on line 9. Since `i` has an initial value of the Integer `3`; the loop will iterate `3` times before ending. The `loop` method returns `nil`.

This example demonstrates local variable scoping rules in Ruby; when a block is passed to a `loop` method invocation; it introduce a new scope. From inside the block, you can access variables that were initialized outside of the block. However, from outside the bock, you can't access any variables that were initialized inside the block.

