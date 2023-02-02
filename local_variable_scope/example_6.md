**What does the following code return? What does it output? Why? What concept does it demonstrate?**

```ruby
arr = [1, 2, 3, 4]
counter = 0
sum = 0

loop do
  sum += arr[counter]
  counter += 1
  break if counter == arr.size
end

puts "Your total is #{sum}"
```

# Written Response:

The local variable `arr` is assigned to the Array `[1, 2, 3, 4]` on line 4. The local variable `counter` is initialized and assigned to the Integer `0` on line 5. The local variable `sum` is initialized and assigned to the Integer `0` on line 6.

The `do...end` alongside the `loop` invocation method on lines 8-12 defines a block, within which the variable `sum` uses the add AND assignment operator to add the integer `0` to the value of each index of the array; starting from the `arr` index of `counter`; on each loop iteration.

The `counter` variable on line 10 uses the add AND assignment operator to add it's initial value `0` to the the Integer `1` on each loop iteration. The `break` condition on line 11 shows the loop will break once `counter` is equal to the size of the `arr`; this is the Integer `4`.

The `puts` method is called on line 14 with a String passed in as an argument; since the String uses interpolation for the variable `sum`; the output is `"Your total is 10"`. 



