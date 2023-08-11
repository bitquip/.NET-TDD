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

## Enhancing the Gear Class with More Tests

As we continue our exploration of Test-Driven Development (TDD), let's extend our tests to cover additional functionalities of the `Gear` class. Through systematic testing and incremental development, we build a solid foundation for our code.

### Testing Pitch Diameter Calculation

Next, we'll write tests to validate the accuracy of the `PitchDiameter` calculation in the `Gear` class.

#### Step 6: Writing Tests for Pitch Diameter Calculation

1. In the `GearTests.cs` file located in the `Tests` folder of your test project, add the following test method:

```csharp
[Theory]
[InlineData(1.5, 10, 20, 15.0)]
[InlineData(2.0, 20, 30, 40.0)]
[InlineData(0.8, 15, 45, 12.0)]
public void GetPitchDiameter_WithModuleAndTeeth_ReturnsCorrectValue(double module, int teeth, double pressureAngle, double expectedPitchDiameter)
{
    // Arrange
    var gear = new Gear(module, teeth, pressureAngle);

    // Act
    var result = gear.PitchDiameter;

    // Assert
    Assert.Equal(expectedPitchDiameter, result, 10);
}
```

Here, we're using the **Theory** attribute again with **InlineData** to test the `PitchDiameter` property with different input values. The test checks whether the calculated pitch diameter matches the expected pitch diameter within a specified tolerance.

### Implementing More Gear Class Functionality

With our new test in place, let's proceed to implement the `PitchDiameter` property in the `Gear` class.

#### Step 7: Implementing the `PitchDiameter` Property

1. Open the `Program.cs` file located in the root directory of your project.

2. Add the implementation for the `PitchDiameter` property in the `Gear` class:

```csharp
public class Gear
{
    // ...

    public double PitchDiameter
    {
        get { return Module * Teeth; }
    }
}
```

Now, the `PitchDiameter` property is calculated as the product of `Module` and `Teeth`.

### Completing the Red-Green-Refactor Cycle

With the implementation in place, let's run our tests again to complete the red-green-refactor cycle.

#### Step 8: Running the Tests Again

1. Navigate back to the root directory of your project (if you are in the `GearCalculator.Tests` folder, use `cd ..`).

2. Run the tests using the following command:

```bash
dotnet test
```

As the tests pass, we have successfully implemented the `PitchDiameter` property using the TDD approach.

---

**You're making great progress!**

By systematically writing tests and implementing code, you're creating a robust application with well-defined functionalities. 

Our journey into TDD and .NET development continues as we explore more aspects of the `Gear` class.

> Moving onward!



<br>
<br>

**Previous: [Writing Another Test](https://bitquip.github.io/.NET-TDD/another)** <space></space> <space></space> &nbsp; &nbsp; &nbsp; &nbsp; &nbsp;&nbsp;&nbsp; **Next: [Evolving Code Through Refactoring](https://bitquip.github.io/.NET-TDD/refactoring)**
