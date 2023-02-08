**What does the following code return? What does it output? Why? What concept does it demonstrate?**

```ruby
def test(b)
  b.map { |letter| "I like the letter: #{letter}" }
end

a = ['a', 'b', 'c']
test(a)

# What is `a`? What if we called `map!` instead of `map`?
```
# Written Response:

The local variable `a` is initialized and assigned to the Array literal `['a', 'b', 'c']` on line 8. The `test` method invocation passes the reference `a` as an argument on line 9.

The `{}` alongside the `map` method invocation defines a block on line 5. Within the block; the parameter `letter` represents the current element of the reference `a`; the block will return a new String on each iteration. The block is passed to `map` as an argument and returns a new Array literal; `["I like the letter: a", "I like the letter: b", "I like the letter: c"]`; this is the return value of the `test` method invocation.

Since `a` is not mutated from inside the method; it returns the original object; the Array literal `['a', 'b', 'c']`.

If we called `map!` instead of `map` this would mutate `a` from inside the method and affect the object outside of the method.

This problem demonstrates the concepts of mutating vs non-mutating methods. `map` is a non-mutating method and returns a new array. When passing a reference into an object and calling a non-mutating method on the object from inside of the method; the original object outside of the method is not affected.

