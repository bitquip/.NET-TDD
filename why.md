<details markdown="block">
   <summary>Table of Contents</summary>
   

1. [Introduction to Test-Driven Development (TDD) in .NET](https://bitquip.github.io/.NET-TDD/introducing)
   - Welcome!
   - Strap in, and off you go!


2. [Why Test-Driven Development?](https://bitquip.github.io/.NET-TDD/why)
   - The Red-Green-Refactor Process
   - Red
   - Green
   - Refactor

  
3. [Getting Started](https://bitquip.github.io/.NET-TDD/started)
   - Prerequisites
   - Setting Up
   - Understanding the setup
  

4. [Writing Tests for the Gear Class](https://bitquip.github.io/.NET-TDD/first)
   - Your First Test: Calculating Base Diameter
     
   - Writing More Tests for the Gear Class
   - Evolving Code Through Test-Driven Refactorings


5. [Adding More Tests](https://bitquip.github.io/.NET-TDD/another)
   - Testing Pitch Calculation
   - Implementing the Gear Class Functionality
   - The Red-Green-Refactor Cycle Continues!

  
6. [Enhancing the Gear Class](https://bitquip.github.io/.NET-TDD/more)
   - Testing Pitch Diameter Calculation
   - Implementing More Gear Class Functionality
   - Nice work!

  
7. [Evolving Code Through Test-Driven Refactorings](https://bitquip.github.io/.NET-TDD/refactoring)
   - Testing New Functionality: Gear Ratio
   - Test-Driven Refactoring


8. [Ensuring Code Quality with Test Coverage](https://bitquip.github.io/.NET-TDD/coverage)
   - Understanding Test Coverage
   - Interpreting the Coverage Report
   - Embracing Test-Driven Development and Test Coverage


9. [Mastering Unit Testing with Test Doubles](https://bitquip.github.io/.NET-TDD/mocks)
   - Introducing Test Doubles
   - Step 14: Using Test Doubles
   - Writing Tests with Mocks
   - Step 15: Writing Tests with Mocks
   - Implementing Code with Mocked Dependencies
   - Step 16: Implementing Code with Mocked Dependencies
   - Embracing Isolation with Test Doubles


10. [Efficient Testing with Parameterized Tests](https://bitquip.github.io/.NET-TDD/parameterized)
   - Introducing Parameterized Tests
   - Step 17: Writing Parameterized Tests
   - Achieving Comprehensive Testing with Efficiency


11. [Organizing Tests with Test Suites](https://bitquip.github.io/.NET-TDD/organization)
   - Introducing Test Suites
   - Step 18: Organizing Tests into Suites


12. [Applying TDD Best Practices](https://bitquip.github.io/.NET-TDD/bestpractices)
   - Real-World TDD: Best Practices and Considerations
   - Step 19: Real-World TDD Best Practices


13. [Conclusion: Your Journey in Test-Driven Development](https://bitquip.github.io/.NET-TDD/conclusion)
    - Congratulations on your hard work!
    - Key Takeaways
    - Continuing your excellence


</details>

---

## Why Test-Driven Development?

![TDD Blueprint](https://miro.medium.com/v2/resize:fit:1400/0*m9IeLR30F2AAtlwu.jpg)

Imagine building a complex structure without a blueprint. The result might be unstable and error-prone. Similarly, in software development, writing code without a clear plan can lead to unforeseen bugs and difficulties.

This is where Test-Driven Development comes into play. TDD is like having a blueprint for your code.

The TDD process involves three fundamental steps:

1. **Write a failing test**

2. **Write the minimum code to make it pass**

3. **Refactor to improve the code without changing its behavior**

**_Let's break down these steps further:_**

### 1. Red: Write a Failing Test

Consider you're an engineer developing plans for an advanced airliner.

Before construction begins, meticulous planning is essential to ensure the final aircraft's excellence. This mirrors the essence of Test-Driven Development (TDD).

The process starts by drafting a test that precisely outlines the desired behavior. Initially, the test purposefully fails since the corresponding code hasn't been generated.

Just as a well-crafted blueprint is vital before building an airliner, the "red" phase highlights the significance of progressing purposefully towards a clear objective.

### 2. Green: Write the Minimum Code

Once your failing test is in place, it's time to write the minimum code necessary to make the test pass.

This step corresponds to assembling the key structural elements of the airliner according to the blueprint.

In TDD, the code is methodically composed to satisfy the test's conditions.

Although not exhaustive, the "green" phase effectively demonstrates the code's ability to fulfill the intended task.

### 3. Refactor: Improve Without Changing Behavior

With the airliner's foundational structure in place, refinement follows. In TDD, this entails improving the code's efficiency without changing its core behavior—akin to optimizing the airliner's design to enhance performance without compromising its original intent.

Through streamlining, optimization, and thoughtful adjustments, the "refactor" phase guarantees code reliability while promoting better organization.

This tutorial will guide you through the principles and practices of TDD while building a .NET Console Application.

You'll witness firsthand how TDD helps us build robust, reliable, and well-tested software.

Let's dive in and explore the world of TDD in .NET development!

<br>

<div style="display: flex; justify-content: center; align-items: center;">
    <a href="https://bitquip.github.io/.NET-TDD/introducing" style="margin: 0 10px; text-decoration: none;">Previous Page</a>
    <span style="margin: 0 10px;">2/10</span>
    <a href="https://bitquip.github.io/.NET-TDD/started" style="position: absolute; bottom: 2px; right: 1px; margin: 0 10px; text-decoration: none;">Next Page</a>
</div>
