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

## Organizing Tests with Test Suites

As our Test-Driven Development (TDD) project grows, it becomes important to keep our tests organized for better maintainability. Test suites allow us to group related tests together and manage our tests more effectively.

### Introducing Test Suites

A test suite is a collection of related test cases that focus on specific functionalities or components. By organizing tests into suites, we can easily identify and run tests associated with specific parts of our application.

#### Step 18: Organizing Tests into Suites

1. In the `GearTests.cs` file located in the `Tests` folder of your test project, let's organize our tests into suites using the `TestClass` attribute:

```csharp
using Xunit;

// ...

public class GearTests
{
    // Test suite for Gear class properties
    [Trait("Category", "Properties")]
    public class PropertiesTests
    {
        // ... Existing property tests here ...
    }

    // Test suite for Gear class methods
    [Trait("Category", "Methods")]
    public class MethodsTests
    {
        // ... Existing method tests here ...
    }

    // Test suite for Gear class with mocked dependencies
    [Trait("Category", "MockedDependencies")]
    public class MockedDependencyTests
    {
        // ... Existing tests with mocks here ...
    }

    // Parameterized test suite for gear calculations
    [Trait("Category", "Calculations")]
    public class CalculationsTests
    {
        // ... Existing parameterized tests here ...
    }
}
```

In this example, we're using nested classes to create test suites based on different categories such as properties, methods, mocked dependencies, and calculations. The `Trait` attribute helps categorize the tests for better organization.

### Managing Complexity with Test Suites

As your codebase expands, maintaining a well-organized suite of tests becomes essential. By grouping tests into logical categories, you can manage complexity and locate specific tests more efficiently.

Congratulations! You've learned how to organize your tests into suites, enhancing the maintainability and manageability of your testing efforts. By categorizing your tests effectively, you're simplifying the process of navigating and running your tests.

Stay engaged as we dive into more advanced TDD topics and continue our exploration of .NET development!
