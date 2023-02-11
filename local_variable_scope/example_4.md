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

The method definition `example` accepts `str` as a parameter on line 4.

The `example` method invocation passes the String literal `'hello'` in as an argument on line 13.

The local variable `i` is initialized and assigned to the Integer `3` on line 5. The `do...end` alongside the `loop` method invocation on lines 6-10 defines a block, within which; the `puts` method invocation passes in the reference of `str` in as an argument which is the String `'hello'`; the output is the String `'hello'` printed on a newline, three times.

Within each iteration of the `loop` method invocation; `i` subtracts the Integer `1` and reassigns the value back to `i` on line 8. The `loop` method will break if `i` is equal to the Integer `0`; as shown on line 9. Since `i` has an initial value of the Integer `3`; the loop will iterate `3` times before breaking. The `loop` method returns `nil`.

The `example` method invocation outputs the String `'hello'` three times, each on a newline, and returns `nil`.

This example demonstrates local variable scoping rules in Ruby; when a block is passed to a `loop` method invocation; it introduce a new scope. From inside the block, you can access variables that were initialized outside of the block. However, from outside the bock, you can't access any variables that were initialized inside the block.

