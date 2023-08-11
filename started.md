## Getting Started

Before we dive into writing code, let's make sure we have everything set up correctly. In this section, we'll cover the prerequisites, set up our project, and get familiar with the provided code.

### Prerequisites

Before we begin, ensure you have the following installed on your development machine:

- [.NET SDK](https://dotnet.microsoft.com/download) - This is the core development platform for building .NET applications. Make sure you have the .NET SDK installed for your platform.

### Setting Up the Project

#### Step 1: Create a New Project Folder

Let's start by creating a dedicated folder for our project. Open your terminal or command prompt and navigate to the directory where you want to create the project folder.

```bash
mkdir GearCalculator
cd GearCalculator
```

#### Step 2: Create the .NET Console Application

Now that we have our project folder ready, let's create a .NET Console Application project. Run the following command:

```bash
dotnet new console -n GearCalculator
```

This command creates a new .NET Console Application project named "GearCalculator" within our project folder.

#### Step 3: Navigate to the Project Directory

Navigate into the newly created project directory:

```bash
cd GearCalculator
```

#### Setup the Gear class

```csharp
using System;

namespace GearCalculator
{
    public class Gear
    {
        // Properties
        public double Module { get; }
        public int Teeth { get; }
        public double PressureAngle { get; }

        // Constructor
        public Gear(double module, int teeth, double pressureAngle)
        {
            Module = module;
            Teeth = teeth;
            PressureAngle = pressureAngle;
        }

        // Methods to calculate properties will be added later
    }

    class Program
    {
        static void Main(string[] args)
        {
            Console.WriteLine("Hello GearCalculator!");
        }
    }
}
```

### Understanding the Provided Code

Our project structure is now set up, and we're ready to dive into the code. Let's take a closer look at the provided code and understand its components.

#### The Gear Class

The `Gear` class is the heart of our application. It represents a single gear and contains properties to store essential information about the gear. These properties include:

- `Module`: The gear's module, which defines the size of the teeth.
- `Teeth`: The number of teeth on the gear.
- `PressureAngle`: The pressure angle of the gear's teeth.

In addition to the properties, the `Gear` class also has methods to calculate various properties of the gear, such as `BaseDiameter`, `Pitch`, and `PitchDiameter`.

#### The Program Class

The `Program` class serves as the entry point for our console application. Currently, it contains a basic `Main` method that prints a simple message. We'll be adding more functionality to this class as we progress through the tutorial.

### Conclusion

In this section, we've prepared our development environment by setting up the necessary prerequisites and creating a .NET Console Application project. We've also explored the provided code and gained an understanding of the `Gear` and `Program` classes.

In the next section, we'll dive into the exciting world of Test-Driven Development (TDD) by writing our first set of tests for the `Gear` class. We'll follow the TDD process to ensure that our code is thoroughly tested and functional.

---

Now that we have a clear understanding of the project setup and the provided code, it's time to start implementing the Test-Driven Development (TDD) approach. TDD is a powerful methodology that guides us in creating robust and reliable code by writing tests before implementing the actual functionality.

### Writing Tests for the Gear Class

In this section, we'll focus on writing tests for the `Gear` class. Our aim is to ensure that the calculations and properties of the `Gear` class work as expected.

#### The Red-Green-Refactor Process

TDD follows an iterative process known as the **Red-Green-Refactor** cycle. This cycle consists of three steps: **Red**, **Green**, and **Refactor**.

1. **Red**: Write a Failing Test  
   In the **Red** phase, we write a test that describes the behavior we want to implement. This test intentionally fails because we haven't written the corresponding code yet. Think of this phase as creating a "blueprint" for the code's functionality.

2. **Green**: Write the Minimum Code  
   In the **Green** phase, we write the minimum code necessary to make the failing test pass. The goal is to implement the functionality indicated by the test without overcomplicating it. This phase is about making the "duct-taped airplane" fly, using the analogy we discussed earlier.

3. **Refactor**: Improve Without Changing Behavior  
   In the **Refactor** phase, we improve the code without altering its behavior. This phase is crucial for enhancing the code's readability, maintainability, and efficiency. We can optimize, organize, and clean up the code to make it better.

### Your First Test: Calculating Base Diameter

Let's start by writing a test for the `BaseDiameter` property of the `Gear` class. The `BaseDiameter` is a crucial calculation that we want to ensure is correct.

#### Step 1: Creating a Test Project

Before we begin writing tests, let's create a separate test project for our unit tests. This isolation helps us maintain a clear separation between the application code and the tests.

1. In your terminal or command prompt, navigate back to the root directory of your project:

```bash
cd ..
```

2. Create a new xUnit test project named "GearCalculator.Tests":

```bash
dotnet new xunit -n GearCalculator.Tests
```

3. Navigate into the test project directory:

```bash
cd GearCalculator.Tests
```

#### Step 2: Writing Your First Test

Let's start by writing your first test for the `Gear` class. Open the `GearTests.cs` file located in the `Tests` folder of your test project.

Replace the existing content with the following code:

```csharp
using Xunit;
using GearCalculator;

namespace GearCalculator.Tests
{
    public class GearTests
    {
        [Fact]
        public void GetBaseDiameter_WithModuleAndTeeth_ReturnsCorrectValue()
        {
            // Arrange
            var gear = new Gear(1.0, 10, 20.0);

            // Act
            var result = gear.BaseDiameter;

            // Assert
            Assert.Equal(4.0808206181339193, result, 10);
        }
    }
}
```

In this test method, we are using the **Fact** attribute provided by the xUnit framework.
The **Fact** attribute denotes that this method is a test and should be executed by the test runner.

Now, let's dive into the Anatomy of a Test, where we break down the **Arrange**, **Act**, and **Assert** steps:

- **Arrange**: In this section, we set up the necessary objects and data for the test. Here, we create an instance of the `Gear` class with specific inputs: a module of `1.0`, `10` teeth, and a pressure angle of `20.0`.

- **Act**: This step involves invoking the method or property that we want to test. In our case, we call the `BaseDiameter` property of the `gear` instance to calculate the base diameter.

- **Assert**: In this part, we verify the results of the test. We use the `Assert.Equal` method to compare the expected base diameter value (`4.0808206181339193`) with the actual result. The third argument, `10`, specifies the maximum allowable difference between the expected and actual values (also known as the tolerance).

In the upcoming sections, we will write more tests for the `Gear` class and implement the corresponding functionality to make the tests pass.

**By following the red-green-refactor cycle, we ensure that our code is thoroughly tested and functional.**
