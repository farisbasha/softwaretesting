# **Part A**

## **1.Explain the differences between Fault, Error, and Bug?**

| Term   | Definition                                              | Example                                    |
|--------|---------------------------------------------------------|--------------------------------------------|
| Fault  | A flaw in the system's code, design, or architecture    | Missing validation check in login process  |
| Error  | Deviation from the intended behavior of the system      | Incorrect calculation in a banking system |
| Bug    | An error or fault that causes unexpected behavior       | Application crashes upon user interaction |

## **2.What are the functions of Test driver and Test stubs in dynamic unit testing?**

| Test Driver                                   | Test Stub                                     |
|-----------------------------------------------|-----------------------------------------------|
| Controls test execution and invokes functions | Simulates behavior of unavailable components |
| Provides input values to the component       | Mimics output of called components            |
| Ensures interaction with other components    | Allows testing of individual units in isolation |
| Handles test setup and teardown activities   | Simplifies integration testing                |
| Used in top-down integration testing         | Used in bottom-up integration testing         |

## **3.What are du paths and du pairs in a data flow graph?**

#### **DU Pair:**
  - A DU pair consists of a definition and use for a variable, where at least one DU path exists from the definition to the use.
  -  For instance, `x = ...` is a definition of variable `x`
  -  `y = ... x ...` is a use of `x`.

 #### **DU Path:** 
  - A DU path is a path in the Control Flow Graph (CFG) starting from a definition of a variable and leading to its use within the program.
  - It represents the flow of data from the point of definition to the point of use. 
  - Definition-clear: A DU path is considered definition-clear if the value of the variable is not replaced or modified along the path.
  - Note: Loops may create infinite DU paths between a definition and a use, requiring careful consideration during analysis.

## **4.Differences between White Box Testing & Grey Box Testing:**

| White Box Testing                               | Grey Box Testing                                     |
|-------------------------------------------------|------------------------------------------------------|
| Tests internal structures, paths, and flows     | Tests focus on functionality, inputs, and outputs   |
| Requires access to the source code              | Can be performed with or without access to the code |
| Checks for code coverage and logic correctness  | Emphasizes on user experience and system behavior   |
| Identifies potential security vulnerabilities   | Identifies integration issues and interoperability  |
| Often used for security and code review         | Commonly applied in penetration testing and QA      |


# **Part B**
