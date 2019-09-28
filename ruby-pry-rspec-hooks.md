## Intro
In this video I will be demonstrating a very powerful tool for developing in Ruby called `pry`. We will also use `pry` to explore the popular assertion library `rspec`. Also I will demonstrate how the use hooks can help organize our test code.

### Demo Description

#### Pry

- Pry is a debugging tool for Ruby, it makes available the method call `binding.pry` Which will use as breakpoint in our code. To understand what pry does first will look at `IRB`.

- IRB stands for 'interactive Ruby'. In the cmd prompt or terminal type `irb`, this opens a REPL session of IRB. In this session we can test Ruby expressions and see what the output will be.

- When a Ruby program is run with a `binding.pry` breakpoint in it, the script will run up to that point and will open and `irb` type session at the breakpoint. Once there all defined objects a variables will be available to experiment with.

- To begin with `pry` we first add it to our Gemfile and run bundle install.

- Then we insert `binding.pry` into our step code and run the test.

- Now we are able access any defined variables and run code inside of pry to test.

Now that we have `pry` installed lets use it to explore some other tools. Using pry can greatly decrease dev time, and in my opinion is a considerable "quality of life" tool that makes Ruby a joy to code in. From here on it you will see me use it often.

#### Rspec

- Rspec is very popular assertion library for Ruby that is mostly used for unit testing rails applications. Rspec comes preloaded with many natural language matchers as well as the ability to define custom matchers and behavior.

- First we add `rspec` to our Gemfile and run bundle install

- Now we are able to set up some rspec assetions

- A basic pattern that is suitable to use in cucumber test is `expect(<EXPRESSION_UNDER_TEST>).to eql(EXPETED_RESULT)`.

- First we have a passing scenario.

- Now we will create a failing scenario to see what `rspec` returns.

- As we can see Rspec's default error is to return the expected and actual return

- For many cases the default return is fine, but sometimes if a test fails you want to surface more information that will be useful to both the tester, and anyone else that will be looking at the test failure reports.

- Rspec supports returning a custom failure string, but only with Rspec's `to_be` matcher.

- To accomplish this in any test the following pattern can be used `expect(<EXPRESSION_UNDER_TEST>).to be(true), "\nYour custom message:\n\n  with #{interpolated values}"` Where the expression under test is Ruby code that will return true or false depending on if there is a pass or fail condition in the test.

- Note the use of line breaks and double spacing, this is purely to make the message more readable which is more important the more data that you wish to return.

- Using the above pattern does require some skill in creating the Ruby expression that will evaluate to true or false so some practice with Ruby evaluation blocks is highly recommended before implementing this pattern. That being said a large project could exist without ever using custom matchers and still be an effective test suite.

### Hooks

- Now lets look at an important feature of cucumber, `hooks`

- Hooks are essentially blocks of code that run before, after, or around step code. When the hook is run is based on where the hook tag is placed in the feature file.

- Hooks can be used to set up and tear down test data, or to instance classes and make them available to your test code as an instance variable.

- For this demo we will define a hook that will make an intance var for our test.

- Hooks must be defined under `features/support` in file such as `hooks.rb`

- Once we have defined the var we will use an rspec expectation and pry to verify the object is available to the test code.
