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

On line 8, the local variable `a` is initialized and assigned to the array `['a', 'b', 'c']`. On line 9, we invoke the `test` method and pass in `a` as an argument.

On line 5, we invoke `map` on the calling object `b` which is bound to the array `['a', 'b', 'c']`; the object that was passed in as an argument to `test` on line 9. After the method invocation of `map` we define a block and pass it in as an argument to the method.

The return value of the method is a new array with the following string objects:
`["I like the letter: a, I like the letter: b, I like the letter: c"]`. 

If we called `map!` instead of `map` we would return the same value from the method but; the original calling object `a` will be permanently modified with same array values.

This problem demonstrates object passing and mutating vs non-mutating methods. Arrays are mutable objects; when arrays are passed into a method as arguments; they can be mutated or not mutated. In this example we can see the difference between a non-mutating method; `.map`; and a mutating method; `.map!`; which have different side-effects on their calling objects.
