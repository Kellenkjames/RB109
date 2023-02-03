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

The local variable `a` is initialized and assigned to the Array `['a', 'b', 'c']` on line 8. The `test` method is called on line 9 and `a` is passed to it as an argument.

The `{}` alongside the `map` method invocation on the local variable `b`; is bound to the Array `['a', 'b', 'c']` and defines a block. Within the block; the parameter `letter` is used to represent each String object in the Array.

The `map` method will return a *new* array with the following value:
`["I like the letter: a", "I like the letter: b", "I like the letter: c"]`

This problem demonstrates object passing. In this example, Ruby acts as "pass-by-value" since the method returns a *new* array and the original object is left unchanged.
