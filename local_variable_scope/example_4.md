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

The method `example` is called on line 13 with the String `'hello'` passed to it as an argument. The local variable `i` is assigned to the Integer `3` on line 5. The `do...end` alongside the `loop` method invocation on lines 6-10 defines a block, within which the `puts` method is called on line 7 and the local variable `str`; which is bound to the String `'hello'`; is passed to it as an argument.

The local variable `i` uses the subtract AND assignment operator on line 8 to subtract the Integer `1` from its initialized value `3` on each iteration. The `loop` will break when the variable `i` is equal to the Integer `0`; this results in `3` loop iterations. The method returns `nil`.

This example demonstrates local variable scoping rules in Ruby; when working with method definitions; the same local variable scoping rules apply; when a variable is initialized from outside of a block; it can be accessed inside the block.


