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

The method definition `test` accepts `b` as a parameter on line 4.

The local variable `a` is initialized and assigned to the Array `['a', 'b', 'c']` on line 8. The `test` method invocation passes in the reference of `a` as an argument on line 9.

The `{}` alongside the `map` method invocation defines a block on line 5. Within the block; the parameter `letter` represents the current element of `a`; the block will be called for each `letter` in `a`. This returns a new Array whose elements are the return values from the block: `["I like the letter: a", "I like the letter: b", "I like the letter: c"]`;

Since `a` is not mutated from inside the method; it returns the original object; the Array `['a', 'b', 'c']`.
The return value of the `test` method invocation is the Array `["I like the letter: a", "I like the letter: b", "I like the letter: c"]`. 

If we called `map!` instead of `map` this would mutate `a` from inside the method and affect the object outside of the method.

This problem demonstrates object passing. In this example, Ruby acts like "pass-by-value". Arrays are mutable objects. Since the original object was passed into the method and a non-mutating method was called on the object; the original object outside of the method was not affected.

