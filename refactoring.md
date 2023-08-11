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

## Evolving Code Through Test-Driven Refactorings

As we progress in our Test-Driven Development (TDD) journey, we'll encounter situations where our code needs improvement. Test-Driven Refactorings allow us to enhance our codebase while maintaining its functionality and ensuring the existing tests still pass.

### Testing New Functionality: Gear Ratio

To demonstrate this concept, we'll add a new functionality to the `Gear` class: calculating the gear ratio. We'll write tests for this new feature and then refactor the code to accommodate it.

#### Step 9: Writing Tests for Gear Ratio Calculation

1. In the `GearTests.cs` file located in the `Tests` folder of your test project, add the following test method:

```csharp
[Theory]
[InlineData(1.5, 10, 20, 0.5)]
[InlineData(2.0, 20, 30, 0.6666666666666666)]
[InlineData(0.8, 15, 45, 0.3333333333333333)]
public void GetGearRatio_WithModuleAndTeeth_ReturnsCorrectValue(double module, int teeth, double pressureAngle, double expectedGearRatio)
{
    // Arrange
    var gear = new Gear(module, teeth, pressureAngle);

    // Act
    var result = gear.GearRatio;

    // Assert
    Assert.Equal(expectedGearRatio, result, 15);
}
```

In this test, we're introducing a new `GearRatio` property and testing its calculation for various inputs using the **Theory** attribute and **InlineData**.

#### Step 10: Implementing the `GearRatio` Property

1. Open the `Program.cs` file located in the root directory of your project.

2. Add the implementation for the `GearRatio` property in the `Gear` class:

```csharp
public class Gear
{
    // ...

    public double GearRatio
    {
        get { return (double)Teeth / Module; }
    }
}
```

The `GearRatio` is calculated as the ratio of `Teeth` to `Module`.

### Test-Driven Refactoring

With the new functionality in place, let's take a moment to perform a test-driven refactoring. This ensures that we maintain our code quality while enhancing its capabilities.

#### Step 11: Running Tests and Refactoring

1. Navigate back to the root directory of your project (if you are in the `GearCalculator.Tests` folder, use `cd ..`).

2. Run the tests using the following command:

```bash
dotnet test
```

Ensure that all tests pass, confirming the correctness of the newly added functionality.

3. Now, let's refine the code to improve readability. In the `Gear` class, update the `GearRatio` property implementation to use a clearer variable name:

```csharp
public double GearRatio
{
    get { return (double)Teeth / Module; }
}
```

With this refactor, we're making the code more understandable and maintaining its functionality.

---

**Congratulations!**

You've successfully evolved your codebase through test-driven refactorings. By adhering to TDD principles, you've ensured that your application remains reliable while accommodating new features.

Stay engaged as we continue to explore advanced TDD concepts and delve deeper into .NET development!
