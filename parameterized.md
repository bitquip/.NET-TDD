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

## Efficient Testing with Parameterized Tests

As we advance in our Test-Driven Development (TDD) journey, we often encounter situations where we need to test the same functionality with multiple input scenarios. Parameterized tests allow us to achieve this efficiently and maintainable.

### Introducing Parameterized Tests

Parameterized tests enable us to write a single test method that can be executed with multiple sets of input data. This approach helps us validate the behavior of our code across different scenarios.

#### Step 17: Writing Parameterized Tests

1. In the `GearTests.cs` file located in the `Tests` folder of your test project, let's create a parameterized test to validate gear calculations with various input data:

```csharp
[Theory]
[InlineData(1.0, 10, 20.0, 4.0808206181339193)]
[InlineData(1.5, 15, 30.0, 7.539822368615503)]
[InlineData(2.0, 20, 45.0, 12.566370614359172)]
public void GearCalculations_ReturnCorrectValues(double module, int teeth, double pressureAngle, double expectedValue)
{
    // Arrange
    var gear = new Gear(module, teeth, pressureAngle);

    // Act
    var baseDiameter = gear.BaseDiameter;
    var pitch = gear.Pitch;
    var pitchDiameter = gear.PitchDiameter;

    // Assert
    Assert.Equal(expectedValue, baseDiameter, 10);
    Assert.Equal(expectedValue, pitch, 10);
    Assert.Equal(expectedValue, pitchDiameter, 10);
}
```

In this parameterized test, we're using the **InlineData** attribute to provide different sets of input data for the `module`, `teeth`, `pressureAngle`, and `expectedValue` parameters. The test method will be executed for each set of data, and the test assertions will validate the calculations.

### Achieving Comprehensive Testing with Efficiency

Parameterized tests allow us to achieve comprehensive testing with minimal code duplication. By testing a wide range of scenarios using a single test method, we ensure the robustness of our codebase.

---

**Yeahhhh!** 

You've unlocked the power of parameterized tests, enabling you to efficiently test your code across various scenarios. By writing tests that cover a multitude of cases, you're increasing the reliability of your application.

Stay engaged as we explore more advanced TDD concepts and dive deeper into .NET development!
