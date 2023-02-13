# Question 1:

This is an example of..

```ruby
MyModule
```
# Your Answer:
B) CamelCase

**Correct**

#_____________________

# Question 2:

Identify the valid Ruby comment style.

# Your Answer:
C

```ruby
# This is a comment
```

**Correct**

#_____________________

# Question 3:

Select all the code examples that are valid examples of Ruby syntax.

# Your Answer:

A)
```ruby
response = Kernel.gets().chomp()
```

B)
```ruby
response = Kernel.gets.chomp
```

D)
```ruby
response = gets.chomp
```

**Correct**

#_____________________

# Question 4:

Examine the following code:

```ruby
a = 2
b = rand(2)
a *= b

if a = 2
  puts 'Two'
else
  puts 'Not Two'
end
```

# There is an error in the code which means that it will always output "Two". Identify the line responsible for the error.

# Your Answer: 
D

```ruby
if a = 2
```

**Correct**

#_____________________

# Question 5:

What is pseudocode?

# Your Answer:

B) Pseudocode is a human-readable, high-level description of a program or algorithm which helps us formulate a solution at the logical problem domain level.

**Correct**

#_____________________

# Question 6: 

Examine the code below:

```ruby
num = 8

if #omitted code
  puts 'Goodbye'
end
```
Which of the following code snippets can replace #omiited code so the code outputs `Goodbye`? Select all that apply. 

# Your Answer: 

A 
```ruby
num > 5 && num < 10
```

B
```ruby
num < 4 || num == 8 && num > 6
```

C
```ruby
num < 7 || num > 7
```

*Incorrect* - D should have been added as an answer (easy fix)

#_____________________

# Question 7: 

Examine the code below:

```ruby
num = 12

if #omitted code
  puts 'Hello'
end
```

Which of the following code snippets can replace `#omitted code` so the code outputs `"Hello"`? Select all that apply.

# Your Answer:

A
```ruby
num / 3 > 3 && num < 10
```

C
```ruby
num % 4 == 0 || num < 7 && num < 10
```

*Incorrect* - C and D are the only correct answers.

#_____________________

# Question 8: 

Given the following piece of pseudocode, which code implementation most closely matches it?

Given a sentence made up of several words, write a method to do the following.

Iterate through the words one by one.
  - save the first word as the starting value.
  - starting with the next word iterate through all the remaining words in the sentence
  - for each iteration, compare the saved value with the current word.
  - if the word is longer or the same length as the saved value:
    - reassign the saved value as the current word
  - move on to the next word

After iterating through the sentence, return the saved value.

# Your Answer: 

C
```ruby
def longest_word(sentence)
  words = sentence.split
  saved_word = words.shift

  words.each do |word|
    if word.length >= saved_word.length
      saved_word = word
    end
  end

  saved_word
end
```

**Correct**

#_____________________

# Question 9: 

In Ruby, what do we mean when we say that an expression evaluates to a truthy value? Choose all the answers that apply.

# Your Answer:

B) It evaluates as true when used in a conditional.

C) It is not `nil` or `false`.

*Incorrect* - Should have added D to the final solution.

#_____________________

# Question 10:

There is an error in the code below; identify what it is.

```ruby
user_input = gets

loop do
  name = user_input
  break
end

if user_input
  puts "Hello " + name
end
```
# Your Answer:

B) The local variable `name` is initialized within the block, and so is not available in the outer scope.

**Correct**

#_____________________

# Question 11:

What specifically do we mean when we refer to a variable's scope?

# Your Answer:

C) We mean where in a program that variable is available for use.

**Correct**

#_____________________

# Question 12:

Select all of the statements which are true regarding local variable scope in Ruby.

# Your Answer: 

A) Methods define their own, self-contained, scope. 

C) Any code delimited by either curly braces `{}` or `do/end` defines a new scope.

D) Variables initialized in an outer scope can be accessed in an inner scope defined by a block, but not vice versa.

*Incorrect* - Only correct answers are `A` and `D`

#_____________________

# Question 13:

Which statement most accurately describes why the last line of the code below outputs "hi"?

```ruby
def extend_greeting(greeting)
  greeting + " there"
end

greeting = "hi"
extend_greeting(greeting)

puts greeting
```

# Your Answer:

C) Because the `String#+` method does not mutate the caller.

**Correct**

#_____________________

# Question 14:

Looking again at the code from the previous question:

```ruby
def extend_greeting(greeting)
  greeting + " there"
end

greeting = "hi"
extend_greeting(greeting)

puts greeting
```

Select all the ways in which we could change this code in order for the last line to output `"hi there".`

# Your Answer:

C) Remove `puts greeting` and change `extend_greeting(greeting)` to `puts extend_greeting(greeting)`.

D) Change `greeting + " there"` to `greeting << " there"`.

*Incorrect* - Missing `B`

#_____________________

# Question 15: 

Which of the following behaviors does Ruby exhibit when passing an object as an argument to a method call? Select all that apply.

# Your Answer: 

A) When an object is passed to a method call as an argument, the parameter assigned to it acts as a pointer to the original object. 

B) Re-assigning a variable within a method doesn't affect the object that the variable is pointing to outside of the method. 

D) It is possible for an operation within the method to mutate the original object outside of the method.

**Correct**

#_____________________

# Question 16: 

What do we mean when we talk about variables as pointers in Ruby? Select all answers that apply.

# Your Answer:

B) Variables in Ruby act as labels we create to refer to physical space in memory. 

**Correct**

#_____________________

# Question 17:

Why is the `name` method invoked instead of the local variable `name` on line 8 in the following example?

```ruby
def name
  "George"
end

name = "Lisa"

def display_name
  puts name
end

display_name
```

# Your Answer:

B) Ruby tries to reference the local variable `name` first, but can't access it from within the method, so the `name` method is invoked instead.

*Incorrect*

#_____________________

# Question 18: 

In the following example, `"George"` is printed to the screen because the name method is invoked on line 8.

```ruby
def name
  "George"
end

name = "Lisa"

def display_name
  puts name()
end

display_name
```

How can we change the code so that `"Lisa"` is printed instead?

# Your Answer:
D
```ruby
def name 
  "George"
end

name = "Lisa"

def display_name(name)
  puts name
end

display_name(name)
```
#_____________________

# Question 19: 

In the following example, why does Ruby reference the local variable `name` on line 8 instead of invoking the `name` method?

```ruby
name = "Lisa"

def name
  "George"
end

loop do
  puts name
  break
end
```

# Your Answer:  A

A) Local variables initialized outside of a block (in the outer scope) can be accessed from within the block's inner scope. Inside the block, both the local variable and the method are in scope, but by default Ruby first references the local variable.


Total Score: 13 (68.42%)



