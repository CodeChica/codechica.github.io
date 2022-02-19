## Why Test Driven Development (TDD)?

Test driven development is the process of writing tests before actually coding anything.
This helps a developer think about the requirements of a feature they're working on before writing the code for it.
You can be more sure that you haven't missed anything important about a feature's needs when you use this process.

Test driven development also makes refactoring much easier because we don't have to worry about breaking any existing code.
If we make changes, and something does change, a test will fail (essentially warning us), and we can make sure everything works again before pushing changes to the main branch of our project.
TDD also helps with better code coverage, which leads to fewer bugs in your application.
Finally, you can look back on your code and know exactly what you were trying to do by reading your tests.

To learn more, read our [Ruby Guide](../../guides/ruby.html)

### Write your first test

When we write tests, we follow the steps of "Red, Green, Refactor".
What this means is, we first write a test for a feature we want to build.
That feature has not been written yet, so our test will fail at first (red).
We write the simplest code to get our test to pass (green), and finally refactor to make our code better.

Use this pattern to get started:

> When \<context\> is established, it \<behavior\>

Example:

> When a sparkle is created, it saves the recipient

> When a sparkle is created, it saves the reason

```rb
require "minitest/autorun"

describe "Sparkle" do
  describe "when a sparkle is created" do
    it "saves the recipient" do
    end
  end
end
```

In order to write our test, we're going to use the pattern "Arrange, Act, Assert".

If you think of putting on a play, first we have the set the stage.

That's our "arrange" in this example:

```rb
require "minitest/autorun"

describe "Sparkle" do
  describe "when a sparkle is created" do
    before do
      # arrange
      @recipient = "@monalisa"
      @reason = "for helping me with my homework!"
    end

    it "saves the recipient" do
    end
  end
end
```

Next, is the "act" portion. We're "acting" upon our variables that we set up earlier.

```rb
require "minitest/autorun"

describe "Sparkle" do
  describe "when a sparkle is created" do
    before do
      # arrange
      @recipient = "@monalisa"
      @reason = "for helping me with my homework!"

      # act
      @sparkle = Sparkle.create(@recipient, @reason)
    end

    it "saves the recipient" do
    end
  end
end
```

Finally, we have "assert" which is checking to see if the result matches what we expect it to be.

```ruby
require "minitest/autorun"

describe Sparkle do
  describe "when a sparkle is created" do
    before do
      # arrange
      @recipient = "@monalisa"
      @reason = "for helping me with my homework!"

      # act
      @sparkle = Sparkle.create(@recipient, @reason)
    end

    it "saves the recipient" do
      # assert
      assert_equal @recipient, @sparkle.sparklee
    end
  end
end
```

Remember, our test won't pass right away because we haven't written the code for the feature yet, but we want to make sure that our test is failing for the right reasons.
From here, you should get a failing test message that looks like:

```bash
Expected: "@monalisa"
  Actual: nil
```

This tells us that our code currently doesn't satisfy the conditions described in the test.

When giving feedback, use the "critique sandwich" method.

1. Say something positive about your partner's code.
1. Give your critiques. What could be better? What do you have questions about?
1. End with another positive!

## Refactor

When you receive notes from your teammates, now is when you can look at how to improve your code.

Keep these things in mind when refactoring:

1. Does your code do what it should do well?
2. KISS (Keep it simple, silly).
3. Functions should be responsible for one thing in general. This is the Single Responsibility Principle (SRP). Do you have any functions that are long and can be broken up in this way?
4. Keep it DRY. DRY stands for "Don't Repeat Yourself". Do you see any code that repeats and could be put into it's own function to simplify your code? If so, go ahead and do that!
5. Keep methods small. Create chunks of code that you can reuse in different places.

None of these are hard and fast rules, so use your best judgement. Ultimately, we should care about "readability". Will you be able to make sense of your code when you come back to it later? Will others be able to understand your code and what it's doing?

### Rinse and repeat

Repeat the peer review and refactor steps until you are happy with the state of your code. Then, start from Step 1 again, and write more tests!

## Conclusion

In this lesson, you learned about test driven development and the reasons for its use. You also learned some intro Ruby concepts in order to get your first suite of tests to pass and to write your own tests. Finally, you practiced peer reviewing someone else's code, and refactoring to make your code better.

{% include youtube.html youtube_id="1_uRNFkFX5Q" %}

